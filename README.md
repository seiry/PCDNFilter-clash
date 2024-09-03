## usage

```yml
rule-providers:
    pcdn:
        type: http
        behavior: classical
        url: https://github.com/seiry/PCDNFilter-clash/raw/main/pcdn.yaml
        path: ./ruleset/pcdn.yaml
        interval: 86400
    cn-doh:
        type: http
        behavior: domain
        url: https://github.com/seiry/PCDNFilter-clash/raw/main/doh.domain.yaml
        path: ./ruleset/cn-doh.yaml
        interval: 86400
```

and 

```yml
rules:
    - RULE-SET, cn-doh, REJECT
    - RULE-SET, pcdn, REJECT
```
