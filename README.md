ansible-es_api_reindex
======================

Use the [Elasticsearch ReIndex API](https://www.elastic.co/guide/en/elasticsearch/reference/current/docs-reindex.html) from Ansible.

Requirements
------------

Ansible 2.x

Role Variables
--------------

|   Variable                         | required | format    | comments                                               |
|------------------------------------|----------|-----------|--------------------------------------------------------|
| es_api_reindex.host                |  yes     | host:port | The elasticsearch host. Port must be included.|
| es_api_reindex.src                 |  yes     |           | The source index.|
| es_api_reindex.dest                |  yes     |           | The destination index.|
| es_api_reindex.url_params          |  no      |           | When defined, will be appended to the request url.|
| es_api_reindex.conflicts           |  no      | bool      | When defined and `true`, will place `"conflicts": "proceed"` into the request body.|
| es_api_reindex.op_type             |  no      | string    | When defined, the value will be inserted into the `op_type` key of the `dest` of the request body.|
| es_api_reindex.query               |  no      | yaml      | A yaml structure which, when defined, will be json-encoded into the `query` key of the `source` of the request body.|


Dependencies
------------

N/A

Example Playbooks
-----------------

See the `reindex_split-by-hour.yml` playbook in this repo.

License
-------

BSD

Author Information
------------------

Jonathan Strootman - jstroot@cyverse.org
