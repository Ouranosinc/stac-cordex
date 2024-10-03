# Template Extension Specification

- **Title:** CORDEX-CMIP6
- **Identifier:** <https://ouranosinc.github.io/stac-cordex/main/json-schema/schema.json>
- **Field Name Prefix:** cordex6
- **Scope:** Item, Collection
- **Extension [Maturity Classification](https://github.com/radiantearth/stac-spec/tree/master/extensions/README.md#extension-maturity):** Proposal
- **Owner**: @huard

This document explains the CORDEX Extension to the [SpatioTemporal Asset Catalog](https://github.com/radiantearth/stac-spec) (STAC) specification.

This extension specifies a set of properties for Coordinated Regional Climate Downscaling Experiment (CORDEX) datasets.

- Examples:
  - [Item: example](examples/item.json): TODO
  - [Collection example](examples/collection.json): TODO
- [JSON Schema](json-schema/schema.json)
- [Changelog](./CHANGELOG.md)

## Fields

The fields in the table below can be used in these parts of STAC documents:

- [ ] Catalogs
- [x] Collections
- [x] Item Properties (incl. Summaries in Collections)
- [x] Assets (for both Collections and Items, incl. Item Asset Definitions in Collections)
- [ ] Links


| Field Name                     | Type    | Description                                                                    |
|--------------------------------|---------|--------------------------------------------------------------------------------|
| cordex6:access                 | array   | e.g. `["HTTPServer"]`                                                          |
| cordex6:activity_id            | string  | e.g. `DD`                                                                      |
| cordex6:citation_url           | string  | e.g. `TODO`                                                                    |
| cordex6:cf_standard_name       | string  | e.g. `air_pressure_at_mean_sea_level`                                          |
| cordex6:creation_date          | string  | e.g. `2024-02-20T19:28:19.804842Z`                                             |
| cordex6:domain_id              | string  | e.g. `NAM-12`                                                                  |
| cordex6:driving_experiment_id  | string  | e.g. `ssp245`                                                                  |
| cordex6:driving_institution_id | string  | e.g. `CCCma`                                                                   |
| cordex6:driving_source_id      | string  | e.g. `CanESM5-1`                                                               |
| cordex6:driving_variant_label  | string  | e.g. `r1i1p1f1`                                                                |
| cordex6:experiment_id          | string  | e.g. `ssp245`                                                                  |
| cordex6:frequency              | string  | e.g. `mon`                                                                     |
| cordex6:further_info_url       | string  | e.g. `https://furtherinfo.es-doc.org/CMIP6.UA.MCM-UA-1-0.ssp245.none.r1i1p1f2` |
| cordex6:grid                   | string  | e.g. `lat-lon`                                                                 |
| cordex6:index_node             | string  | e.g. `null`                                                                    |
| cordex6:instance_id            | string  | e.g. `CMIP6.ScenarioMIP.UA.MCM-UA-1-0.ssp245.r1i1p1f2.Amon.psl.gn.v20190731`   |
| cordex6:institution_id         | string  | e.g. `UA`                                                                      |
| cordex6:latest                 | boolean | e.g. `true`                                                                    |
| cordex6:license                | string  | e.g. `CMIP6`                                                                   |
| cordex6:mip_era                | string  | e.g. `CMIP6`                                                                   |
| cordex6:nominal_resolution     | string  | e.g. `250 km`                                                                  |
| cordex6:pid                    | string  | e.g. `null`                                                                    |
| cordex6:product                | string  | e.g. `model-output`                                                            |
| cordex6:project_id             | string  | e.g. `CORDEX`                                                                  |
| cordex6:replica                | boolean | e.g. `false`                                                                   |
| cordex6:retracted              | boolean | e.g. `false`                                                                   |
| cordex6:source_id              | string  | e.g. `MCM-UA-1-0`                                                              |
| cordex6:source_type            | string  | e.g. `AOGCM`                                                                   |
| cordex6:sub_experiment_id      | string  | e.g. `none`                                                                    |
| cordex6:table_id               | string  | e.g. `Amon`                                                                    |
| cordex6:tracking_id            | string  | e.g. `hdl:21.14100/7f3e1e7d-6b0b-4b7b-8b3d-3b1f7f4b4b1e`                       |  
| cordex6:updated                | string  | e.g. `2024-02-20T19:28:19.804842Z`                                             |
| cordex6:variable_id            | string  | e.g. `psl`                                                                     |
| cordex6:variable_long_name     | string  | e.g. `Sea Level Pressure`                                                      |
| cordex6:variable_units         | string  | e.g. `Pa`                                                                      |
|cordex6:version_realization | string | e.g. `v20190731` |


### Additional Field Information

#### template:new_field

This is a much more detailed description of the field `template:new_field`...

### XYZ Object

This is the introduction for the purpose and the content of the XYZ Object...

| Field Name | Type   | Description                                  |
| ---------- | ------ | -------------------------------------------- |
| x          | number | **REQUIRED**. Describe the required field... |
| y          | number | **REQUIRED**. Describe the required field... |
| z          | number | **REQUIRED**. Describe the required field... |

## Relation types

The following types should be used as applicable `rel` types in the
[Link Object](https://github.com/radiantearth/stac-spec/tree/master/item-spec/item-spec.md#link-object).

| Type           | Description                           |
| -------------- | ------------------------------------- |
| fancy-rel-type | This link points to a fancy resource. |

## Contributing

All contributions are subject to the
[STAC Specification Code of Conduct](https://github.com/radiantearth/stac-spec/blob/master/CODE_OF_CONDUCT.md).
For contributions, please follow the
[STAC specification contributing guide](https://github.com/radiantearth/stac-spec/blob/master/CONTRIBUTING.md) Instructions
for running tests are copied here for convenience.

### Running tests

The same checks that run as checks on PR's are part of the repository and can be run locally to verify that changes are valid. 
To run tests locally, you'll need `npm`, which is a standard part of any [node.js installation](https://nodejs.org/en/download/).

First you'll need to install everything with npm once. Just navigate to the root of this repository and on 
your command line run:
```bash
npm install
```

Then to check markdown formatting and test the examples against the JSON schema, you can run:
```bash
npm test
```

This will spit out the same texts that you see online, and you can then go and fix your markdown or examples.

If the tests reveal formatting problems with the examples, you can fix them with:
```bash
npm run format-examples
```
