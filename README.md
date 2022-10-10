# DNS API

This project aims to create a REST API for [BIND DNS](https://www.isc.org/bind/), the Internet's de-facto DNS software, using [Dnspython](https://www.dnspython.org/), a DNS toolkit for Python. It is useful for queries, zone transfers, dynamic updates, nameserver testing, and a variety of other tasks.

Dnspython provides both high and low level DNS access. The high level classes search for data by name, type, and class and return an answer set. The low-level classes allow for the manipulation of DNS zones, messages, names, and records directly. Almost every RR type is supported.

dnspython was created at [Nominum](https://www.nominum.com)where to test DNS nameservers.

While we in search for  the tool kit for developing this API we have inspired by [this great project](https://gitlab.com/jaytuck/bind-rest-api) where it has used FastAPI Python  framework to develop an API for BIND DNS. 

# About FastAPI 

<p align="center">
  <a href="https://fastapi.tiangolo.com"><img src="https://fastapi.tiangolo.com/img/logo-margin/logo-teal.png" alt="FastAPI"></a>
</p>

---

**Documentation**: <a href="https://fastapi.tiangolo.com" target="_blank">https://fastapi.tiangolo.com</a>

**Source Code**: <a href="https://github.com/tiangolo/fastapi" target="_blank">https://github.com/tiangolo/fastapi</a>

---

FastAPI is a modern, fast (high-performance), web framework for building APIs with Python 3.7+ based on standard Python type hints.

The key features are:

* **Fast**: Very high performance, on par with **NodeJS** and **Go** (thanks to Starlette and Pydantic). [One of the fastest Python frameworks available](#performance).
* **Fast to code**: Increase the speed to develop features by about 200% to 300%. *
* **Fewer bugs**: Reduce about 40% of human (developer) induced errors. *
* **Intuitive**: Great editor support. <abbr title="also known as auto-complete, autocompletion, IntelliSense">Completion</abbr> everywhere. Less time debugging.
* **Easy**: Designed to be easy to use and learn. Less time reading docs.
* **Short**: Minimize code duplication. Multiple features from each parameter declaration. Fewer bugs.
* **Robust**: Get production-ready code. With automatic interactive documentation.
* **Standards-based**: Based on (and fully compatible with) the open standards for APIs: <a href="https://github.com/OAI/OpenAPI-Specification" class="external-link" target="_blank">OpenAPI</a> (previously known as Swagger) and <a href="https://json-schema.org/" class="external-link" target="_blank">JSON Schema</a>.

<small>* estimation based on tests on an internal development team, building production applications.</small>

# Core Feature of BIND API

This is a BIND API that supports the following core functions and others:

* It can  export a BIND  zone file to a JSON  file
* It utilises the HTTP GET method to locate a specific DNS record.
* It utilises the HTTP PUT  method to replace or update a DNS record
* It utilises the HTTP DELETE method for deleting a DNS record
* It safeguards the API Key. 
* Ii offers an audit log for 'apikey' to 'DNS changes.'
* It makes use of the [acme.sh](https://acme.sh) tool kit to generate LetsEncrypt certificates via the API.
* It can be installed in a Docker container to make it easier to run in any environment that supports Docker.

## Auto-generated API documents

This project receives auto-generated Swagger-UI documentation by using FastAPI: 

Please take a look at the screenshots below.

## Getting set up and running

Please see BIND API documentation[bindapi.apititan.works](https://bindapi.apititan.works) for a detailed DNS API user guide.

