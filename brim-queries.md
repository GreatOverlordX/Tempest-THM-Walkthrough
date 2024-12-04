# Brim 
## Queries roadmap

*This is a guide for myself **OR** for yourself even*

* to get all `HTTP` requests related to a malicious C2 traffic:
    - `_path=="http" "<replace domain>" id.resp_p==<replace port> | cut ts, host, id.resp_p, uri | sort ts`


* get `HTTP` requests related to a malicious C2 traffic
    
    - `_path=="http" "<replace domain>" id.resp_p==<replace port> | cut ts, host, id.resp_p, uri | sort ts`

