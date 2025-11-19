---
title: jq_examples
created: 2025-10-21
modified: 2025-10-21
---

ddgr Using jq
youtube-dl --skip-download --print-json "$(xclip -o)"|jq '{"date": .upload_date,"title": .title,"URL": .url,"duration": .duration}'\
man jq
cat example.json|jq .[].
cat example.json|jq ".[]."
cat example.json|jq .
cat example.json|jq .
cat example.json|jq .|grep upload
cat example.json|jq .|jq
cat example.json|jq .|jq '.[].'
cat example.json|jq '.[].'
cat example.json | jq '.[].'
cat example.json | jq '.[].upload'
cat example.json |jq .|grep upload
cat example.json | jq '.[].upload_date'
jq --version
cat example.json | jq '.'
cat example.json | jq -c '.'
cat example.json | jq -c '.[]'
jq '.' example.json
jq '.' example.json|grep upload
jq '.[]|.upload_date' example.json
jq '.[] | .upload_date' example.json
jq '.[] | upload_date' example.json
jq '.[] | .upload_date' example.json
jq '.' example.json|grep upload
jq '.' example.json|grep upload_d
jq '.' example.json
jq ' .[] ' example.json
jq ' .[] |.upload_date ' example.json
jq ' .[] |.upload_date ' example.json|less
jq '.' example.json
jq '.' example.json|less
jq '.' example.json
ddgr list json keys with jq
cat example.json|jq -n 'inputs[] | keys[] | unique'
jq -n 'inputs[] | keys[] | unique' example.json
jq -n 'inputs[] | keys[] | unique' example.json
jq -r
jq -r . JP_n_Jim.json
jq -r . JP_n_Jim.json|grep upload
jq -r .upload_date JP_n_Jim.json
cat example.json|jq .|grep upload
cat example.json|jq .|grep upload
cat example.json|jq .upload_date
cat example.json|jq .title .upload_date
cat example.json|jq .title | .upload_date
cat example.json|jq '.title | .upload_date'
cat example.json|jq .title .upload_date
cat example.json|jq .title
cat example.json|jq -r .title
cat example.json|jq keys[]
jq keys[] example.json
jq 'keys[]' example.json
jq '.is_live' example.json
jq '.tags' example.json
jq -r '.tags' example.json
jq -r '.tags' example.json
jq 'keys[]' example.json
jq '.channel_id' example.json
jq 'inputs[]' example.json
jq '.channel_url' example.json
jq '.uploaded_ur\
jq '.uploader_url' example.json
jq '[].uploader_url' example.json
jq '[.].uploader_url' example.json
jq '.uploader_url|.upload_date' example.json
jq '.[]| .uploader_url' example.json
jq '.| .uploader_url' example.json
jq '.| .uploader_url | .upload_id' example.json
jq '.| .uploader_url,.upload_id' example.json
jq '.| .uploader_url,.upload_date' example.json
jq '.| .title,.upload_date' example.json
jq -r '.| .title,.upload_date' example.json
jq '.uploader_url|.upload_date' example.json
jq '.uploader_url,.upload_date' example.json
jq '.uploader_url|.upload_date' Ride-NaruCptuelM.info.json
jq '.uploader_url|.upload_date' Sticks\ First\ Ride-NaruCptuelM.info.json
jq 'keys[]' Sticks\ First\ Ride-NaruCptuelM.info.json
jq 'keys[]' Sticks\ First\ Ride-NaruCptuelM.info.json|grep up
jq '|.upload_date' Sticks\ First\ Ride-NaruCptuelM.info.json
jq '.upload_date' Sticks\ First\ Ride-NaruCptuelM.info.json
jq '|.upload_date' Sticks\ First\ Ride-NaruCptuelM.info.json
jq 'keys[]' Sticks\ First\ Ride-NaruCptuelM.info.json|grep up
jq '.title' Sticks\ First\ Ride-NaruCptuelM.info.json
jq '.title,.upload_date' Sticks\ First\ Ride-NaruCptuelM.info.json
youtube-dl --skip-download --print-json "$(xclip -o)"|jq -r '.title,.upload_date'
youtube-dl --skip-download --print-json "$(xclip -o)"|jq -r '.title,.upload_date,.url'
youtube-dl --skip-download --print-json "$(xclip -o)"|jq -r 'keys[]'
youtube-dl --skip-download --print-json "$(xclip -o)"|jq -r '.title,.upload_date,.webpage_url'
youtube-dl --skip-download --print-json "$(xclip -o)"|jq -r '.title,.upload_date,.uploader_url'
youtube-dl --skip-download --print-json "$1" |jq -r '.title,.upload_date,.uploader_url'
youtube-dl --skip-download --print-json "$1" |jq -r '.title,.upload_date,.uploader_url'
echo "youtube-dl --skip-download --print-json \"$1\" |jq -r '.title,.upload_date,.uploader_url'" >> ytupdate.sh
echo "youtube-dl --skip-download --print-json \"$1\" |jq -r '.title,.upload_date,.uploader_url'" >> ~/bin/ytupdate.sh
echo "youtube-dl --skip-download --print-json \"$1\" |jq -r '.title,.upload_date,.uploader_url'" >> ~/bin/ytupdate.sh
echo "youtube-dl --skip-download --print-json $1 |jq -r '.title,.upload_date,.uploader_url'" >> ~/bin/ytupdate.sh
cat .zsh_history|grep jq
cat .zsh_history|grep jq|uniq
cat .zsh_history|grep jq|uniq > ~/zets/202207192250-jq_examples.md
