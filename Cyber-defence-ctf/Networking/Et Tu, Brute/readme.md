Suspicious traffic has been seen on our company web server. Can you figure out the type of attack and find the flag?

The flag in this one is not in the usual `leveleffect{FLAG}` format. You'll know it when you find it. When you do, submit it in the format `leveleffect{INSERT_FLAG_HERE}`
![[http-traffic.pcap]]

# Method:

Used wireshark on the file and found that the packets show the same username being used and then constant password attempts.

The first attempts were even sql injection attempts

flag attempts

leveleffect{Password_attacks}

leveleffect{SQL_injection_attacks}

leveleffect{password_spray_attacks}

leveleffect{brute_force_attacks}

leveleffect{http-post-form_attack}

leveleffect{http_post_form_attack}

leveleffect{http_post_form}

leveleffect{Denial_of_service_attack}

leveleffect{web_application_attack}

leveleffect{active_attack}

leveleffect{Injection_Attacks}

leveleffect{Fuzz}

leveleffect{Web_attacks}

leveleffect{Credential_stuffing}

leveleffect{Credential_stuffing_attack}

leveleffect{dictionary_attack}

After much effort trying to brute force the flag i instead just looked at the packets themselves.

![[The flag.png]]

This is what the flag looks like in packet 2739

I managed to find it by looking up how to filter correctly via chat gpt

It told me to filter http.request.method = "POST" which filters it to only the packets that attempted the brute force attack.

Then i quickly went through them for anything odd.

flag = leveleffect{y0u-kn0w-h77p-r3qu3575}