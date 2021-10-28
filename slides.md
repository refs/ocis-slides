---
theme: 'default'
colorSchema: 'dark'
routerMode: 'history'
aspectRatio: '16/9'
fonts:
  sans: 'Roboto'
  serif: 'Roboto Slab'
  mono: 'Fira Code'
---

# oCIS
## A sea of storages

---

# Requirements

- Feature parity with OwnCloud 10, easy to adopt
- Use Go (and Protobufs), ~~easy~~ set in stone contracts
- Microservices, easy to decouple
- Single binary, easy to run
- CS3APIs, easy to scale
- Traces, easy to debug

---

# Challenges

- Wrapping [go-micro](https://github.com/asim/go-micro)
  - Flags duplication, need to be known at runtime
- Configuration
  - Support for multiple sources (config file, cli flags, env variables)
  - Sane defaults
- Custom runtime
  - Supervision tree ([suture](github.com/thejerf/suture)), borrowed from erlang
- Test suite
  - Luxury of having a testsuite inherited from OwnCloud 10 to work with, done by JankariTech

---

# Collaboration

- We are not alone in this, CERN joined forces with us through the [CS3 API]()
- Reference implementation in github.com/cs3org/reva
  - this is where we contribute the most.
- CERN storage team is currently running oCIS + Reva in production.

---

# Roadmap to GA

