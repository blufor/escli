escli
=====

ElasticSearch CLI tool for human beings (i.e. sysadmins)


    Usage:
      escli [-j] index list [<regex>]
      escli [-j] index delete <regex>
      escli [-j] index open <regex>
      escli [-j] index close <regex>
      escli [-j] index optimize <regex> # TBD
      escli [-j] index refresh <regex> # TBD
      escli [-j] index flush <regex> # TBD
      escli [-j] index get-mapping <index>
      escli [-j] index put-mapping <index> # TBD
      escli [-j] index clear-cache [-d [<fields>]] [-c] [-i] [<index>]  # TBD
      escli [-j] template list
      escli [-j] template get <template> # TBD
      escli [-j] template put <template> <file> # TBD
      escli [-j] cluster get-settings # TBD
      escli [-j] cluster put-settings # TBD
      escli [-j] cluster shutdown [<nodes>] # TBD
      escli [-j] cluster status # TBD
      escli [-j] cluster health
