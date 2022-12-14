# ð Awesome TTRSS

![Docker Pulls](https://img.shields.io/docker/pulls/wangqiru/ttrss.svg)
![Docker Stars](https://img.shields.io/docker/stars/wangqiru/ttrss.svg)
![Docker Automated build](https://img.shields.io/docker/automated/wangqiru/ttrss.svg)
![Docker Build Status](https://img.shields.io/docker/build/wangqiru/ttrss.svg)
![FOSSA Status](https://app.fossa.com/api/projects/git%2Bgithub.com%2FHenryQW%2FAwesome-TTRSS.svg?type=shield)

## å³äº

[Tiny Tiny RSS](https://tt-rss.org/) æ¯ä¸æ¬¾åºäº PHP çåè´¹å¼æº RSS èåéè¯»å¨ãð Awesome TTRSS æ¨å¨æä¾ä¸ä¸ª **ãä¸ç«å¼å®¹å¨åã** ç Tiny Tiny RSS è§£å³æ¹æ¡ï¼éè¿æä¾ç®æçé¨ç½²æ¹å¼ä»¥åä¸äºé¢å¤æä»¶ï¼ä»¥æåç¨æ·ä½éªã

## é¸£è°¢

[![èµå©è](https://opencollective.com/awesome-ttrss/backers.svg)](https://opencollective.com/awesome-ttrss#support)

## é¨ç½²

æ¨èä½¿ç¨ä¸å° VPS æ¥é¨ç½²æ¨ç Awesome TTRSS å®ä¾ï¼[DigitalOcean](https://m.do.co/c/d6ef3c80105c) æä¾é«æ§ä»·æ¯ç VPS ä»é \$5/æãé¤æ­¤ä¹å¤ï¼éè¿ Awesome TTRSS ç [ð°OpenCollective é¡µé¢](https://opencollective.com/Awesome-TTRSS/) è¿è¡èµå©ï¼å³å¯è·å¾å®å¶æ¯æï¼å¨æç®¡æå¡ï¼å¨æç®¡ VPS ç­ç§äººæå¡ã

Awesome TTRSS æ¯æå¤æ¶æ <Badge text="x86 â" vertical="top" type="tip"/><Badge text="arm32v7 â" vertical="top" type="tip"/><Badge text="arm64v8 â" vertical="top" type="tip"/>ï¼æä¸åæ¬ OpenCC APIï¼ã

### éè¿ Docker é¨ç½²

```bash
docker run -it --name ttrss --restart=always \
-e SELF_URL_PATH=[ TTRSS å®ä¾å°å ]  \
-e DB_HOST=[ æ°æ®åºå°å ]  \
-e DB_PORT=[ æ°æ®åºç«¯å£ ]  \
-e DB_NAME=[ æ°æ®åºåç§° ]  \
-e DB_USER=[ æ°æ®åºç¨æ·å ]  \
-e DB_PASS=[ æ°æ®åºå¯ç  ]  \
-p [ å®¹å¨å¯¹å¤æ å°ç«¯å£ ]:80  \
-d wangqiru/ttrss
```

### éè¿ docker-compose é¨ç½²

[docker-compose.yml](https://github.com/HenryQW/Awesome-TTRSS/blob/main/docker-compose.yml) åå«äº 4 ä¸ªéåï¼

1. [TTRSS](https://hub.docker.com/r/wangqiru/ttrss)
1. [PostgreSQL](https://hub.docker.com/_/postgres)
1. [Mercury Parser API](https://hub.docker.com/r/wangqiru/mercury-parser-api)
1. [OpenCC API](https://hub.docker.com/r/wangqiru/opencc-api-server) <Badge text="arm32v7 â" vertical="top" type="error"/><Badge text="arm64v8 â" vertical="top" type="error"/>

#### æ­¥éª¤

1. ä¸è½½ [docker-compose.yml](https://github.com/HenryQW/Awesome-TTRSS/blob/main/docker-compose.yml) è³ä»»æç®å½ã
1. æ´æ¹ `docker-compose.yml` ä¸­çè®¾ç½®ï¼è¯·å¡å¿æ´æ¹ postgres ç¨æ·å¯ç ã
1. éè¿ç»ç«¯å¨åç®å½ä¸è¿è¡ `docker-compose up -d` åç­å¾é¨ç½²å®æã
1. é»è®¤éè¿ 181 ç«¯å£è®¿é® TTRSSï¼é»è®¤è´¦æ·ï¼`admin` å¯ç ï¼`password`ï¼è¯·ç¬¬ä¸æ¶é´æ´æ¹ã
1. `wangqiru/mercury-parser-api` å `wangqiru/opencc-api-server` ä¸ºæ¯æé«çº§åè½èå å¥çå¯éæå¡ç±»å®¹å¨ï¼å é¤ä¸ä¼å½±å TTRSS åºç¡åè½ã

### æ¯æçç¯å¢åéåè¡¨

- SELF_URL_PATH: TTRSS å®ä¾å°åã**ð´ è¯·æ³¨æï¼è¯¥åéå¼å¿é¡»ä¸ä½ å¨æµè§å¨ä¸­ç¨äºè®¿é® TTRSS ç URL ä¿æå®å¨ä¸è´ï¼å¦å TTRSS å°æ æ³å¯å¨ã**
- DB_HOST: æ°æ®åºå°å
- DB_PORT: æ°æ®åºç«¯å£
- DB_NAME: æ°æ®åºåå­
- DB_USER: æ°æ®åºç¨æ·å
- DB_PASS: æ°æ®åºå¯ç 
- DB_USER_FILE: Docker Secrets æ¯æï¼æ¿ä»£ DB_USEï¼ï¼åå«æ°æ®åºç¨æ·åçæä»¶
- DB_PASS_FILE: Docker Secrets æ¯æï¼æ¿ä»£ DB_PASSï¼ï¼åå«æ°æ®åºå¯ç çæä»¶
- ENABLE_PLUGINS: å¨å±å¯ç¨çæä»¶åç§°ï¼å¶ä¸­ `auth_internal` ä¸ºå¿é¡»å¯ç¨çç»å½æä»¶
- ALLOW_PORTS: éå·åéç«¯å£å·ï¼å¦`1200,3000`ãåè®¸è®¢éé 80,443 ç«¯å£çæºã**ð´ è°¨æä½¿ç¨ã**
- SESSION_COOKIE_LIFETIME: ä½¿ç¨ç½é¡µçç»éæ¶ cookie è¿ææ¶é´ï¼åä½ä¸ºå°æ¶ï¼é»è®¤ä¸º `24` å°æ¶
- HTTP_PROXY: `ip:port`, TTRSS å®ä¾çå¨å±ä»£çï¼ä¸ºæºå°åæ·»å åç¬ä»£çè¯·ä½¿ç¨ [Options per Feed](#options-per-feed)
- DISABLE_USER_IN_DAYS: å½ç¨æ· X å¤©åæ²¡æç»å½åï¼åæ­¢ä¸ºå¶èªå¨æ´æ°è®¢éæºï¼ç´è³ç¨æ·åæ¬¡ç»é
- FEED_LOG_QUIET: true ç¦ç¨è®¢éæºæ´æ°æäº§ççæ¥å¿æå°

æ´å¤ç¯å¢åéï¼åè§ [å®æ¹ tt-rss](https://git.tt-rss.org/fox/tt-rss/src/branch/master/classes/config.php)ã

### éç½® HTTPS

TTRSS å®¹å¨èªèº«ä¸è´è´£ä½¿ç¨ HTTPS å å¯éä¿¡ãåè§ä¸æ¹çæ ·ä¾èªè¡éç½® Caddy æ Nginx ååä»£çãä½¿ç¨ [Let's Encrypt](https://letsencrypt.org/) å¯ä»¥è·ååè´¹ SSL è¯ä¹¦ã

```nginx
# Caddyfile
ttrssdev.henry.wang {
    reverse_proxy 127.0.0.1:181
    encode zstd gzip
}
```

```nginx
# nginx.conf
upstream ttrssdev {
    server 127.0.0.1:181;
}

server {
    listen 80;
    server_name  ttrssdev.henry.wang;
    return 301 https://ttrssdev.henry.wang$request_uri;
}

server {
    listen 443 ssl;
    gzip on;
    server_name  ttrssdev.henry.wang;

    ssl_certificate /etc/letsencrypt/live/ttrssdev.henry.wang/fullchain.pem;
    ssl_certificate_key /etc/letsencrypt/live/ttrssdev.henry.wang/privkey.pem;

    location / {
        proxy_redirect off;
        proxy_pass http://ttrssdev;

        proxy_set_header  Host                $http_host;
        proxy_set_header  X-Real-IP           $remote_addr;
        proxy_set_header  X-Forwarded-Ssl     on;
        proxy_set_header  X-Forwarded-For     $proxy_add_x_forwarded_for;
        proxy_set_header  X-Forwarded-Proto   $scheme;
        proxy_set_header  X-Frame-Options     SAMEORIGIN;

        client_max_body_size        100m;
        client_body_buffer_size     128k;

        proxy_buffer_size           4k;
        proxy_buffers               4 32k;
        proxy_busy_buffers_size     64k;
        proxy_temp_file_write_size  64k;
    }
}
```

**ð´ è¯·æ³¨æï¼ [ä½ éè¦æ´æ° `SELF_URL_PATH` ç¯å¢åéã](#supported-environment-variables)**

## æ´æ°

Awesome TTRSS ä¼èªå¨çæ§ TTRSS å®æ¹æ´æ°å¹¶ä¸ä¹åæ­¥ï¼è¿æå³çæ´æ°ä¼æ¯è¾é¢ç¹ã

[TTRSS å®æ¹ä¸åéåº tag](https://community.tt-rss.org/t/versioning-changes-for-trunk/2974)ã `wangqiru/ttrss:latest` ä¼ä¸ [å®æ¹ main branch](https://git.tt-rss.org/fox/tt-rss) åæ­¥ã

### æå¨æ´æ°

éè¿ä»¥ä¸å½ä»¤è¿è¡æå¨æ´æ°ï¼

```bash
    docker pull wangqiru/ttrss:latest
    # docker pull wangqiru/mercury-parser-api:latest
    # docker pull wangqiru/opencc-api-server:latest
    docker-compose up -d # å¦ææ¨æ²¡æä½¿ç¨ docker-composeï¼æç¡®ä¿¡æ¨ç¥éè¯¥æä¹åã
```

### èªå¨æ´æ°

[æ ·ä¾ docker-compose](#éè¿-docker-compose-é¨ç½²ï¼ ä¸­åå«äº [Watchtower](https://github.com/containrrr/watchtower)ï¼å®ä¼èªå¨æåå¹¶æ´æ°æ¨ææçæå¡å®¹å¨ ï¼åæ¬å½åç³»ç»ä¸è¿è¡çé Awesome TTRSS æå¡çå®¹å¨ï¼ãè¯¥æå¡é»è®¤å³é­ï¼**å¯ç¨åè¯·ç¡®è®¤å®å°ä¸ä¼å½±åæ¨å¶ä»çæå¡å®¹å¨ã**

æ¨ä¹å¯ä»¥è®¾ç½® watchtower å¿½ç¥æ¨çå¶ä»å®¹å¨ï¼

```yml
service.mercury:
  image: wangqiru/mercury-parser-api:latest
  container_name: mercury
  expose:
    - 3000
  restart: always
  # â¬ï¸ è¿å°ä½¿ Watchtower è·³è¿å¯¹ mercury-parser-api çæ´æ°æ£æµ
  labels:
    - com.centurylinklabs.watchtower.enable=false
```

## æ°æ®åºæ´æ°æè¿ç§»

Postgres å¤§çæ¬æ´æ° (13->14) éè¦é¢å¤çæ­¥éª¤æ¥ç¡®ä¿æå¡æ­£å¸¸è¿è¡ã
ä¸ºäºæ´å¥½å°ä¼å Awesome TTRSSï¼ææ¶åå¯è½ä¼æ¨åºä¸äºç ´åæ§æ´æ°ã

### æ­¥éª¤

è¿äºæ­¥éª¤æ¼ç¤ºäºå¦ä½è¿è¡ Postgres å¤§çæ¬æ´æ°ï¼ä» 12.x è³ 13.xï¼ï¼æèä»å¶ä»éåè¿ç§»è³ postgres:alpineã

1. åæ­¢æææå¡å®¹å¨ï¼

   ```bash
   docker-compose stop
   ```

1. å¤å¶ Postgres æ°æ®å· `~/postgres/data/`ï¼æèä½ å¨ docker-compose ä¸­æå®çç®å½ï¼è³å¶ä»ä»»ä½å°æ¹ä½ä¸ºå¤ä»½ï¼è¿éå¸¸éè¦ï¼
1. æ§è¡å¦ä¸å½ä»¤æ¥å¯¼åºæææ°æ®ï¼

   ```bash
   docker exec postgres pg_dumpall -c -U æ°æ®åºç¨æ·å > export.sql
   ```

1. å é¤ Postgres æ°æ®å· `~/postgres/data/`ã
1. æ ¹æ®ææ° [docker-compose.yml](https://github.com/HenryQW/Awesome-TTRSS/blob/main/docker-compose.yml) ä¸­ç`database.postgres` é¨ä»½æ¥æ´æ°ä½ ç docker-compose æä»¶ï¼**æ³¨æ `DB_NAME` ä¸å¯æ´æ¹**ï¼ï¼å¹¶å¯å¨ï¼

   ```bash
   docker-compose up -d
   ```

1. æ§è¡å¦ä¸å½ä»¤æ¥å¯¼å¥æææ°æ®ï¼

   ```bash
   cat export.sql | docker exec -i postgres psql -U æ°æ®åºç¨æ·å
   ```

1. æµè¯æææå¡æ¯å¦æ­£å¸¸å·¥ä½ï¼ç°å¨ä½ å¯ä»¥ç§»é¤æ­¥éª¤äºä¸­çå¤ä»½äºã

## æä»¶

### [Mercury å¨æè·å](https://github.com/HenryQW/mercury_fulltext)

å¨æåå®¹æåæä»¶ï¼éååç¬ç Mercury Parser API æå¡å¨ä½¿ç¨ã[æ ·ä¾ docker-compose](#éè¿-docker-compose-é¨ç½²ï¼ ä¸­å·²ç»åå«äº [HenryQW/mercury-parser-api](https://github.com/HenryQW/mercury-parser-api) æå¡å¨ã

#### è®¾ç½®æ­¥éª¤

1. å¨è®¾ç½®ä¸­å¯ç¨ `mercury-fulltext` æä»¶
   ![å¯ç¨ Mercury](https://share.henry.wang/92AGp5/x9xYB93cnX+)
1. å¨è®¾ç½®ä¸­å¡«å¥ Mercury Parser API å°å
   ![å¡«å¥ Mercury Parser API å°å](https://share.henry.wang/9HJemY/BlTnDhuUGC+)

ä½¿ç¨ Awesome-TTRSS é¨ç½²ç mercury å¯å¡«å`service.mercury:3000`ã

#### å¨ææåæé®

<img src="https://share.henry.wang/ubHtDz/uxyKk68jqY+" width="400">

### [Fever API](https://github.com/DigitalDJ/tinytinyrss-fever-plugin)

æä¾ Fever API æ¯æã

#### è®¾ç½®æ­¥éª¤

1. å¨è®¾ç½®ä¸­å¯ç¨ APIã
   ![å¯ç¨ API](https://share.henry.wang/X2AnXi/bVVDg9mGDm+)
1. å¨æä»¶è®¾ç½®ä¸­è®¾ç½® Fever å¯ç ã
   ![è®¾ç½® Fever å¯ç ](https://share.henry.wang/HspODo/xRSbZQheVN+)
1. å¨æ¯æ Fever çéè¯»å¨ç¨ï¼ä½¿ç¨ `https://[æ¨çå°å]/plugins/fever` ä½ä¸ºæå¡å¨å°åãä½¿ç¨æ¨çè´¦å·åæ­¥éª¤ 2 ä¸­çå¯ç ç»å½ã
1. ç±äºè¯¥æä»¶ä½¿ç¨æªå çç MD5 å å¯å¯ç è¿è¡éä¿¡ï¼å¼ºçå»ºè®® [å¼å¯ HTTPS](#éç½®-https)ã

### [OpenCC ç¹ç®è½¬æ¢](https://github.com/HenryQW/ttrss_opencc) <Badge text="arm32v7 â" vertical="top" type="error"/><Badge text="arm64v8 â" vertical="top" type="error"/>

ä½¿ç¨ [OpenCC](https://github.com/BYVoid/OpenCC) ä¸º TTRSS æä¾ä¸­æç¹è½¬ç®çæä»¶ï¼éè¦éååç¬ç OpenCC API æå¡å¨ä½¿ç¨ã[æ ·ä¾ docker-compose](#éè¿-docker-compose-é¨ç½²ï¼ ä¸­å·²ç»åå«äº [HenryQW/OpenCC.henry.wang](https://github.com/HenryQW/OpenCC.henry.wang) æå¡å¨ã

#### è®¾ç½®æ­¥éª¤

1. å¨è®¾ç½®ä¸­å¯ç¨ `opencc` æä»¶
   ![å¯ç¨ opencc](https://share.henry.wang/EvN5Nl/2RHNnMV2iP+)
1. å¨è®¾ç½®ä¸­å¡«å¥ OpenCC API å°å
   ![å¡«å¥ OpenCC API å°å](https://share.henry.wang/pePHAz/oWXX3I18hW+)

ä½¿ç¨ Awesome-TTRSS é¨ç½²ç OpenCC å¯å¡«å`service.opencc:3000`ã

#### è½¬æ¢æé®

<img src="https://share.henry.wang/30kbTr/lSaHKXk5NT+" width="400">

### [FeedReader API](https://github.com/jangernert/FeedReader/tree/master/data/tt-rss-feedreader-plugin)

æä¾ FeedReader API æ¯æã

ç³»ç»æä»¶ï¼å° `api_feedreader` æ·»å å° **ENABLE_PLUGINS** ç¯å¢åéä¸­ä»¥å¯ç¨ã

ä½¿ç¨æåè§ [FeedReader API](https://github.com/jangernert/FeedReader/tree/master/data/tt-rss-feedreader-plugin)ã

### [News+ API](https://github.com/voidstern/tt-rss-newsplus-plugin/)

ä¸º Android App [News+](http://github.com/noinnion/newsplus/) å iOS App [Fiery Feeds](http://cocoacake.net/apps/fiery/) æä¾æ´å¿«çåæ­¥éåº¦ã

ç³»ç»æä»¶ï¼å° `api_newsplus` æ·»å å° **ENABLE_PLUGINS** ç¯å¢åéä¸­ä»¥å¯ç¨ã

ä½¿ç¨æåè§ [News+ API](https://github.com/voidstern/tt-rss-newsplus-plugin/)ã

### [Feediron](https://github.com/feediron/ttrss_plugin-feediron)

æä¾æç«  DOM ææ§è½åçæä»¶ã

ä½¿ç¨æåè§ [Feediron](https://github.com/feediron/ttrss_plugin-feediron)ã

### [Options per Feed](https://github.com/sergey-dryabzhinsky/options_per_feed)

æä¾åç¬ä¸ºæºå°åéç½®ä»£çãuser-agent ä»¥å SSL è¯ä¹¦éªè¯çè½åã

ä½¿ç¨æåè§ [Options per Feed](https://github.com/sergey-dryabzhinsky/options_per_feed)ã

### [Wallabag v2](https://github.com/joshp23/ttrss-to-wallabag-v2)

ä¿å­æç« è³ Wallabagã

ä½¿ç¨æåè§ [Wallabag v2](https://github.com/joshp23/ttrss-to-wallabag-v2)ã

### [Remove iframe sandbox](https://github.com/DIYgod/ttrss-plugin-remove-iframe-sandbox)

::: warning æ³¨æ

è¯¥æä»¶ä¸ `Fever API` ä¸è½åæ¶ä½ä¸ºå¨å±æä»¶å¯ç¨ãå¦ææ¨åæ¶éè¦ä¸¤èï¼

1. å¨ç¯å¢åé `ENABLE_PLUGINS` ä¸­ç§»é¤ `fever` å¹¶æ·»å  `remove_iframe_sandbox` ä½ä¸ºå¨å±æä»¶å¯ç¨ã
1. å¨ç»é TTRSS åï¼éè¿è®¾ç½®å° `Fever API` ä½ä¸ºæ¬å°æä»¶å¯ç¨ã

:::

ç§»é¤ iframe ä¸ç sandbox å±æ§ï¼ä»¥æ¯æ feed ä¸­ç´æ¥æ­æ¾åµå¥è§é¢ã

ä½¿ç¨æåè§ [Remove iframe sandbox](https://github.com/DIYgod/ttrss-plugin-remove-iframe-sandbox)ã

## ä¸»é¢

### [Feedly](https://github.com/levito/tt-rss-feedly-theme)

![Feedly](https://share.henry.wang/f3WNje/Q7RoLBSUFp+)

### [RSSHub](https://github.com/DIYgod/ttrss-theme-rsshub)

![RssHub](https://share.henry.wang/E5Lifa/1ykvdTWuew+)

## ä½¿ç¨å»ºè®®

- æ¨èä½¿ç¨ [RSSHub](https://docs.rsshub.app/) æ¥åç°æ´å¤æè¶£çè®¢éæºã
- å¯¹äº iOS å macOS ç¨æ·ï¼åç½®ç [Fever API æ¨¡ææä»¶](#fever-api) æä¾ [Reeder 5](http://reederapp.com/) åç«¯æ¯æã
- å¯¹äº Linux ç¨æ·ï¼åç½®ç [FeedReader API](#feedreader-api) æä¾ [FeedReader](https://jangernert.github.io/FeedReader/) åç«¯æ¯æã

## æ¯æä¸å¸®å©

- éè¿ Awesome TTRSS ç [ð°OpenCollective é¡µé¢](https://opencollective.com/Awesome-TTRSS/) è¿è¡èµå©ï¼å³å¯è·å¾ç§äººå®å¶æ¯æã
- éè¯»æ­¤ [æå](https://henry.wang/2018/04/25/ttrss-docker-plugins-guide.html) å¯è½ä¼æå¸®å©ã
- éè¿ [GitHub issue](https://github.com/HenryQW/Awesome-TTRSS/issues) æäº¤é®é¢ã
- [ç´æ¥æå©æ¯æ](https://tt-rss.org/)ã

## æèµ 

| PayPal                                                                                                                                                                       | å¾®ä¿¡èµèµ                                                            | OpenCollective                                                     |
| ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------- | ------------------------------------------------------------------ |
| [![paypal](https://www.paypalobjects.com/en_US/GB/i/btn/btn_donateCC_LG.gif)](https://www.paypal.com/cgi-bin/webscr?cmd=_s-xclick&hosted_button_id=MTM5L6T4PHRQS&source=url) | <img src="https://share.henry.wang/IKaxAW/duFgAuOnmk+" width="200"> | [ð°OpenCollective page](https://opencollective.com/Awesome-TTRSS/) |

## è®¸å¯

MIT

[![FOSSA Status](https://app.fossa.com/api/projects/git%2Bgithub.com%2FHenryQW%2FAwesome-TTRSS.svg?type=large)](https://app.fossa.com/projects/git%2Bgithub.com%2FHenryQW%2FAwesome-TTRSS?ref=badge_large)
