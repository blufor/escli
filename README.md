escli
=====

ElasticSearch CLI tool for human beings (i.e. sysadmins)

      Usage:
        escli [-j] index list [<regex>]
        escli [-j] index delete <regex>
        escli [-j] index open <regex>
        escli [-j] index close <regex>
        escli [-j] index optimize <regex>
        escli [-j] index refresh <regex>
        escli [-j] index flush <regex>
        escli [-j] index dump <regex> [-g] [--scroll=<time>] [--docs=<docs>]
        escli [-j] index get-mapping <index>
        escli [-j] index put-mapping <index> <file>
        escli [-j] index get-settings <index>
        escli [-j] index put-settings <index> <file>
        escli [-j] index clear-cache [-d [<fields>]] [-c] [-i] [<index>]
        escli [-j] template list
        escli [-j] template get <template>
        escli [-j] template put <template> <file>
        escli [-j] cluster get-settings
        escli [-j] cluster put-settings <file>
        escli [-j] cluster nodes
        escli [-j] cluster routing <index>
        escli [-j] cluster reroute-shard <index> [--shard=<shard>] --from=<from> --to=<to>
        escli [-j] cluster reroute-node <node> --from=<from> --to=<to>
        escli [-j] cluster shutdown [<nodes>]
        escli [-j] cluster health
        escli (-h|--help)
      
      Index Actions:
        list              Lists indices Can be filtered by regex.
        delete            Deletes index/indices by regex. Try regex first on listing!
        open              Opens closed index/indices by regex.
        close             Closes index/indices by regex.
        optimize          Optimizes index/indices by regex.
        refresh           Refreshes index/indices by regex.
        flush             Flushes index/indices by regex.
        dump              Exports mapping, settings and data from index/indices.
                          by regex into directory set in .escli.
        get-mapping       Fetch mapping for index.
        put-mapping       Set new mapping for index from file. `-` is STDIN.
        get-settings      Fetch setting for index.
        put-settings      Set new settings for index from file. `-` is STDIN.
        clear-cache       Clear cache for index.
      
      Template Actions:
        list              List templates.
        get               Fetch template by its name.
        put               Set template by name.
      
      Cluster Actions:
        get-settings      Fetch cluster settings.
        put-settings      Set cluster parameters from file. `-` is STDIN
        nodes
        routing           Show shard routing for index
        reroute-shard     Move index shard to another node
        reroute-node      Move all shards of indexes mathing regex to another node
        shutdown          Shutdown cluster/nodes!
        health            Display cluster health.
      
      Options:
        -h --help         Show this.
        -j                Show output in JSON instead of YAML.
        -g                Dump to gzipped files.
        --scroll=<time>   Time to keep scroll_id in ElasticSearch [default: 30m].
        --docs=<docs>     Number of documents to dump in one chunk [default: 1000].
        --shard=<shard>   Shard id to reroute
        --from=<node>     Node from which to move the shard
        --to=<node>       Node to which to move the shard   