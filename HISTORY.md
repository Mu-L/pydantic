<!-- markdownlint-disable no-bare-urls -->
<!-- markdownlint-disable-next-line first-line-heading -->

## v2.12.0a1 (2025-07-26)

[GitHub release](https://github.com/pydantic/pydantic/releases/tag/v2.12.0a1)

This is the first alpha release of the upcoming 2.12 release, which adds initial support for Python 3.14.

### What's Changed

#### New Features

* Add `__pydantic_on_complete__()` hook that is called once model is fully ready to be used by @DouweM in [#11762](https://github.com/pydantic/pydantic/pull/11762)
* Add initial support for Python 3.14 by @Viicos in [#11991](https://github.com/pydantic/pydantic/pull/11991)
* Add regex patterns to JSON schema for `Decimal` type by @Dima-Bulavenko in [#11987](https://github.com/pydantic/pydantic/pull/11987)
* Add support for `doc` attribute on dataclass fields by @Viicos in [#12077](https://github.com/pydantic/pydantic/pull/12077)
* Add experimental `MISSING` sentinel by @Viicos in [#11883](https://github.com/pydantic/pydantic/pull/11883)

#### Changes

* Allow config and bases to be specified together in `create_model()` by @Viicos in [#11714](https://github.com/pydantic/pydantic/pull/11714)
* Move some field logic out of the `GenerateSchema` class by @Viicos in [#11733](https://github.com/pydantic/pydantic/pull/11733)
* Always make use of `inspect.getsourcelines()` for docstring extraction on Python 3.13 and greater by @Viicos in [#11829](https://github.com/pydantic/pydantic/pull/11829)
* Only support the latest Mypy version by @Viicos in [#11832](https://github.com/pydantic/pydantic/pull/11832)
* Do not implicitly convert after model validators to class methods by @Viicos in [#11957](https://github.com/pydantic/pydantic/pull/11957)
* Refactor `FieldInfo` creation implementation by @Viicos in [#11898](https://github.com/pydantic/pydantic/pull/11898)
* Make `Secret` covariant by @bluenote10 in [#12008](https://github.com/pydantic/pydantic/pull/12008)
* Emit warning when field-specific metadata is used in invalid contexts by @Viicos in [#12028](https://github.com/pydantic/pydantic/pull/12028)

#### Fixes

* Properly fetch plain serializer function when serializing default value in JSON Schema by @Viicos in [#11721](https://github.com/pydantic/pydantic/pull/11721)
* Remove generics cache workaround by @Viicos in [#11755](https://github.com/pydantic/pydantic/pull/11755)
* Remove coercion of decimal constraints by @Viicos in [#11772](https://github.com/pydantic/pydantic/pull/11772)
* Fix crash when expanding root type in the mypy plugin by @Viicos in [#11735](https://github.com/pydantic/pydantic/pull/11735)
* Only mark model as complete once all fields are complete by @DouweM in [#11759](https://github.com/pydantic/pydantic/pull/11759)
* Do not provide `field_name` in validator core schemas by @DouweM in [#11761](https://github.com/pydantic/pydantic/pull/11761)
* Fix issue with recursive generic models by @Viicos in [#11775](https://github.com/pydantic/pydantic/pull/11775)
* Fix qualified name comparison of private attributes during namespace inspection by @karta9821 in [#11803](https://github.com/pydantic/pydantic/pull/11803)
* Make sure Pydantic dataclasses with slots and `validate_assignment` can be unpickled by @Viicos in [#11769](https://github.com/pydantic/pydantic/pull/11769)
* Traverse `function-before` schemas during schema gathering by @Viicos in [#11801](https://github.com/pydantic/pydantic/pull/11801)
* Fix check for stdlib dataclasses by @Viicos in [#11822](https://github.com/pydantic/pydantic/pull/11822)
* Check if `FieldInfo` is complete after applying type variable map by @Viicos in [#11855](https://github.com/pydantic/pydantic/pull/11855)
* Do not delete mock validator/serializer in `model_rebuild()` by @Viicos in [#11890](https://github.com/pydantic/pydantic/pull/11890)
* Rebuild dataclass fields before schema generation by @Viicos in [#11949](https://github.com/pydantic/pydantic/pull/11949)
* Always store the original field assignment on `FieldInfo` by @Viicos in [#11946](https://github.com/pydantic/pydantic/pull/11946)
* Do not use deprecated methods as default field values by @Viicos in [#11914](https://github.com/pydantic/pydantic/pull/11914)
* Allow callable discriminator to be applied on PEP 695 type aliases by @Viicos in [#11941](https://github.com/pydantic/pydantic/pull/11941)
* Suppress core schema generation warning when using `SkipValidation` by @ygsh0816 in [#12002](https://github.com/pydantic/pydantic/pull/12002)
* Do not emit typechecking error for invalid `Field()` default with `validate_default` set to `True` by @Viicos in [#11988](https://github.com/pydantic/pydantic/pull/11988)
* Refactor logic to support Pydantic's `Field()` function in dataclasses by @Viicos in [#12051](https://github.com/pydantic/pydantic/pull/12051)

#### Packaging

* Update project metadata to use PEP 639 by @Viicos in [#11694](https://github.com/pydantic/pydantic/pull/11694)
* Bump `mkdocs-llmstxt` to v0.2.0 by @Viicos in [#11725](https://github.com/pydantic/pydantic/pull/11725)
* Bump `pydantic-core` to v2.35.1 by @Viicos in [#11963](https://github.com/pydantic/pydantic/pull/11963)
* Bump dawidd6/action-download-artifact from 10 to 11 by @dependabot[bot] in [#12033](https://github.com/pydantic/pydantic/pull/12033)
* Bump astral-sh/setup-uv from 5 to 6 by @dependabot[bot] in [#11826](https://github.com/pydantic/pydantic/pull/11826)
* Update mypy to 1.17.0 by @Viicos in [#12076](https://github.com/pydantic/pydantic/pull/12076)

### New Contributors

* @parth-paradkar made their first contribution in [#11695](https://github.com/pydantic/pydantic/pull/11695)
* @dqkqd made their first contribution in [#11739](https://github.com/pydantic/pydantic/pull/11739)
* @fhightower made their first contribution in [#11722](https://github.com/pydantic/pydantic/pull/11722)
* @gbaian10 made their first contribution in [#11766](https://github.com/pydantic/pydantic/pull/11766)
* @DouweM made their first contribution in [#11759](https://github.com/pydantic/pydantic/pull/11759)
* @bowenliang123 made their first contribution in [#11719](https://github.com/pydantic/pydantic/pull/11719)
* @rawwar made their first contribution in [#11799](https://github.com/pydantic/pydantic/pull/11799)
* @karta9821 made their first contribution in [#11803](https://github.com/pydantic/pydantic/pull/11803)
* @jinnovation made their first contribution in [#11834](https://github.com/pydantic/pydantic/pull/11834)
* @zmievsa made their first contribution in [#11861](https://github.com/pydantic/pydantic/pull/11861)
* @Otto-AA made their first contribution in [#11860](https://github.com/pydantic/pydantic/pull/11860)
* @ygsh0816 made their first contribution in [#12002](https://github.com/pydantic/pydantic/pull/12002)
* @lukland made their first contribution in [#12015](https://github.com/pydantic/pydantic/pull/12015)
* @Dima-Bulavenko made their first contribution in [#11987](https://github.com/pydantic/pydantic/pull/11987)
* @GSemikozov made their first contribution in [#12050](https://github.com/pydantic/pydantic/pull/12050)
* @hannah-heywa made their first contribution in [#12082](https://github.com/pydantic/pydantic/pull/12082)

## v2.11.7 (2025-06-14)

[GitHub release](https://github.com/pydantic/pydantic/releases/tag/v2.11.7)

### What's Changed

#### Fixes

* Copy `FieldInfo` instance if necessary during `FieldInfo` build by @Viicos in [#11898](https://github.com/pydantic/pydantic/pull/11898)

## v2.11.6 (2025-06-13)

[GitHub release](https://github.com/pydantic/pydantic/releases/tag/v2.11.6)

### What's Changed

#### Fixes

* Rebuild dataclass fields before schema generation by @Viicos in [#11949](https://github.com/pydantic/pydantic/pull/11949)
* Always store the original field assignment on `FieldInfo` by @Viicos in [#11946](https://github.com/pydantic/pydantic/pull/11946)

## v2.11.5 (2025-05-22)

[GitHub release](https://github.com/pydantic/pydantic/releases/tag/v2.11.5)

### What's Changed

#### Fixes

* Check if `FieldInfo` is complete after applying type variable map by @Viicos in [#11855](https://github.com/pydantic/pydantic/pull/11855)
* Do not delete mock validator/serializer in `model_rebuild()` by @Viicos in [#11890](https://github.com/pydantic/pydantic/pull/11890)
* Do not duplicate metadata on model rebuild by @Viicos in [#11902](https://github.com/pydantic/pydantic/pull/11902)

## v2.11.4 (2025-04-29)

[GitHub release](https://github.com/pydantic/pydantic/releases/tag/v2.11.4)

### What's Changed

#### Packaging

* Bump `mkdocs-llmstxt` to v0.2.0 by @Viicos in [#11725](https://github.com/pydantic/pydantic/pull/11725)

#### Changes

* Allow config and bases to be specified together in `create_model()` by @Viicos in [#11714](https://github.com/pydantic/pydantic/pull/11714).
  This change was backported as it was previously possible (although not meant to be supported)
  to provide `model_config` as a field, which would make it possible to provide both configuration
  and bases.

#### Fixes

* Remove generics cache workaround by @Viicos in [#11755](https://github.com/pydantic/pydantic/pull/11755)
* Remove coercion of decimal constraints by @Viicos in [#11772](https://github.com/pydantic/pydantic/pull/11772)
* Fix crash when expanding root type in the mypy plugin by @Viicos in [#11735](https://github.com/pydantic/pydantic/pull/11735)
* Fix issue with recursive generic models by @Viicos in [#11775](https://github.com/pydantic/pydantic/pull/11775)
* Traverse `function-before` schemas during schema gathering by @Viicos in [#11801](https://github.com/pydantic/pydantic/pull/11801)

## v2.11.3 (2025-04-08)

[GitHub release](https://github.com/pydantic/pydantic/releases/tag/v2.11.3)

### What's Changed

#### Packaging

* Update V1 copy to v1.10.21 by @Viicos in [#11706](https://github.com/pydantic/pydantic/pull/11706)

#### Fixes

* Preserve field description when rebuilding model fields by @Viicos in [#11698](https://github.com/pydantic/pydantic/pull/11698)

## v2.11.2 (2025-04-03)

[GitHub release](https://github.com/pydantic/pydantic/releases/tag/v2.11.2)

### What's Changed

#### Fixes

* Bump `pydantic-core` to v2.33.1 by @Viicos in [#11678](https://github.com/pydantic/pydantic/pull/11678)
* Make sure `__pydantic_private__` exists before setting private attributes by @Viicos in [#11666](https://github.com/pydantic/pydantic/pull/11666)
* Do not override `FieldInfo._complete` when using field from parent class by @Viicos in [#11668](https://github.com/pydantic/pydantic/pull/11668)
* Provide the available definitions when applying discriminated unions by @Viicos in [#11670](https://github.com/pydantic/pydantic/pull/11670)
* Do not expand root type in the mypy plugin for variables by @Viicos in [#11676](https://github.com/pydantic/pydantic/pull/11676)
* Mention the attribute name in model fields deprecation message by @Viicos in [#11674](https://github.com/pydantic/pydantic/pull/11674)
* Properly validate parameterized mappings by @Viicos in [#11658](https://github.com/pydantic/pydantic/pull/11658)

## v2.11.1 (2025-03-28)

[GitHub release](https://github.com/pydantic/pydantic/releases/tag/v2.11.1)

### What's Changed

#### Fixes

* Do not override `'definitions-ref'` schemas containing serialization schemas or metadata by @Viicos in [#11644](https://github.com/pydantic/pydantic/pull/11644)

## v2.11.0 (2025-03-27)

[GitHub release](https://github.com/pydantic/pydantic/releases/tag/v2.11.0)

### What's Changed

Pydantic v2.11 is a version strongly focused on build time performance of Pydantic models (and core schema generation in general).
See the [blog post](https://pydantic.dev/articles/pydantic-v2-11-release) for more details.

#### Packaging

* Bump `pydantic-core` to v2.33.0 by @Viicos in [#11631](https://github.com/pydantic/pydantic/pull/11631)

#### New Features

* Add `encoded_string()` method to the URL types by @YassinNouh21 in [#11580](https://github.com/pydantic/pydantic/pull/11580)
* Add support for `defer_build` with `@validate_call` decorator by @Viicos in [#11584](https://github.com/pydantic/pydantic/pull/11584)
* Allow `@with_config` decorator to be used with keyword arguments by @Viicos in [#11608](https://github.com/pydantic/pydantic/pull/11608)
* Simplify customization of default value inclusion in JSON Schema generation by @Viicos in [#11634](https://github.com/pydantic/pydantic/pull/11634)
* Add `generate_arguments_schema()` function by @Viicos in [#11572](https://github.com/pydantic/pydantic/pull/11572)

#### Fixes

* Allow generic typed dictionaries to be used for unpacked variadic keyword parameters by @Viicos in [#11571](https://github.com/pydantic/pydantic/pull/11571)
* Fix runtime error when computing model string representation involving cached properties and self-referenced models by @Viicos in [#11579](https://github.com/pydantic/pydantic/pull/11579)
* Preserve other steps when using the ellipsis in the pipeline API by @Viicos in [#11626](https://github.com/pydantic/pydantic/pull/11626)
* Fix deferred discriminator application logic by @Viicos in [#11591](https://github.com/pydantic/pydantic/pull/11591)

### New Contributors

* @cmenon12 made their first contribution in [#11562](https://github.com/pydantic/pydantic/pull/11562)
* @Jeukoh made their first contribution in [#11611](https://github.com/pydantic/pydantic/pull/11611)

## v2.11.0b2 (2025-03-17)

[GitHub release](https://github.com/pydantic/pydantic/releases/tag/v2.11.0b2)

### What's Changed

#### Packaging

* Bump `pydantic-core` to v2.32.0 by @Viicos in [#11567](https://github.com/pydantic/pydantic/pull/11567)

#### New Features

* Add experimental support for free threading by @Viicos in [#11516](https://github.com/pydantic/pydantic/pull/11516)

#### Fixes

* Fix `NotRequired` qualifier not taken into account in stringified annotation by @Viicos in [#11559](https://github.com/pydantic/pydantic/pull/11559)

### New Contributors

* @joren485 made their first contribution in [#11547](https://github.com/pydantic/pydantic/pull/11547)

## v2.11.0b1 (2025-03-06)

[GitHub release](https://github.com/pydantic/pydantic/releases/tag/v2.11.0b1)

### What's Changed

#### Packaging

* Add a `check_pydantic_core_version()` function by @Viicos in https://github.com/pydantic/pydantic/pull/11324
* Remove `greenlet` development dependency by @Viicos in https://github.com/pydantic/pydantic/pull/11351
* Use the `typing-inspection` library by @Viicos in https://github.com/pydantic/pydantic/pull/11479
* Bump `pydantic-core` to `v2.31.1` by @sydney-runkle in https://github.com/pydantic/pydantic/pull/11526

#### New Features

* Support unsubstituted type variables with both a default and a bound or constraints by @FyZzyss in https://github.com/pydantic/pydantic/pull/10789
* Add a `default_factory_takes_validated_data` property to `FieldInfo` by @Viicos in https://github.com/pydantic/pydantic/pull/11034
* Raise a better error when a generic alias is used inside `type[]` by @Viicos in https://github.com/pydantic/pydantic/pull/11088
* Properly support PEP 695 generics syntax by @Viicos in https://github.com/pydantic/pydantic/pull/11189
* Properly support type variable defaults by @Viicos in https://github.com/pydantic/pydantic/pull/11332
* Add support for validating v6, v7, v8 UUIDs by @astei in https://github.com/pydantic/pydantic/pull/11436
* Improve alias configuration APIs by @sydney-runkle in https://github.com/pydantic/pydantic/pull/11468

#### Changes

* Rework `create_model` field definitions format by @Viicos in https://github.com/pydantic/pydantic/pull/11032
* Raise a deprecation warning when a field is annotated as final with a default value by @Viicos in https://github.com/pydantic/pydantic/pull/11168
* Deprecate accessing `model_fields` and `model_computed_fields` on instances by @Viicos in https://github.com/pydantic/pydantic/pull/11169
* **Breaking Change:** Move core schema generation logic for path types inside the `GenerateSchema` class by @sydney-runkle in https://github.com/pydantic/pydantic/pull/10846
* Remove Python 3.8 Support by @sydney-runkle in https://github.com/pydantic/pydantic/pull/11258
* Optimize calls to `get_type_ref` by @Viicos in https://github.com/pydantic/pydantic/pull/10863
* Disable `pydantic-core` core schema validation by @sydney-runkle in https://github.com/pydantic/pydantic/pull/11271

#### Performance

* Only evaluate `FieldInfo` annotations if required during schema building by @Viicos in https://github.com/pydantic/pydantic/pull/10769
* Improve `__setattr__` performance of Pydantic models by caching setter functions by @MarkusSintonen in https://github.com/pydantic/pydantic/pull/10868
* Improve annotation application performance by @Viicos in https://github.com/pydantic/pydantic/pull/11186
* Improve performance of `_typing_extra` module by @Viicos in https://github.com/pydantic/pydantic/pull/11255
* Refactor and optimize schema cleaning logic by @Viicos in https://github.com/pydantic/pydantic/pull/11244
* Create a single dictionary when creating a `CoreConfig` instance by @sydney-runkle in https://github.com/pydantic/pydantic/pull/11384
* Bump `pydantic-core` and thus use `SchemaValidator` and `SchemaSerializer` caching by @sydney-runkle in https://github.com/pydantic/pydantic/pull/11402
* Reuse cached core schemas for parametrized generic Pydantic models by @MarkusSintonen in https://github.com/pydantic/pydantic/pull/11434

#### Fixes

* Improve `TypeAdapter` instance repr by @sydney-runkle in https://github.com/pydantic/pydantic/pull/10872
* Use the correct frame when instantiating a parametrized `TypeAdapter` by @Viicos in https://github.com/pydantic/pydantic/pull/10893
* Infer final fields with a default value as class variables in the mypy plugin by @Viicos in https://github.com/pydantic/pydantic/pull/11121
* Recursively unpack `Literal` values if using PEP 695 type aliases by @Viicos in https://github.com/pydantic/pydantic/pull/11114
* Override `__subclasscheck__` on `ModelMetaclass` to avoid memory leak and performance issues by @Viicos in https://github.com/pydantic/pydantic/pull/11116
* Remove unused `_extract_get_pydantic_json_schema()` parameter by @Viicos in https://github.com/pydantic/pydantic/pull/11155
* Improve discriminated union error message for invalid union variants by @Viicos in https://github.com/pydantic/pydantic/pull/11161
* Unpack PEP 695 type aliases if using the `Annotated` form by @Viicos in https://github.com/pydantic/pydantic/pull/11109
* Add missing stacklevel in `deprecated_instance_property` warning by @Viicos in https://github.com/pydantic/pydantic/pull/11200
* Copy `WithJsonSchema` schema to avoid sharing mutated data by @thejcannon in https://github.com/pydantic/pydantic/pull/11014
* Do not cache parametrized models when in the process of parametrizing another model by @Viicos in https://github.com/pydantic/pydantic/pull/10704
* Add discriminated union related metadata entries to the `CoreMetadata` definition by @Viicos in https://github.com/pydantic/pydantic/pull/11216
* Consolidate schema definitions logic in the `_Definitions` class by @Viicos in https://github.com/pydantic/pydantic/pull/11208
* Support initializing root model fields with values of the `root` type in the mypy plugin by @Viicos in https://github.com/pydantic/pydantic/pull/11212
* Fix various issues with dataclasses and `use_attribute_docstrings` by @Viicos in https://github.com/pydantic/pydantic/pull/11246
* Only compute normalized decimal places if necessary in `decimal_places_validator` by @misrasaurabh1 in https://github.com/pydantic/pydantic/pull/11281
* Add support for `validation_alias` in the mypy plugin by @Viicos in https://github.com/pydantic/pydantic/pull/11295
* Fix JSON Schema reference collection with `"examples"` keys by @Viicos in https://github.com/pydantic/pydantic/pull/11305
* Do not transform model serializer functions as class methods in the mypy plugin by @Viicos in https://github.com/pydantic/pydantic/pull/11298
* Simplify `GenerateJsonSchema.literal_schema()` implementation by @misrasaurabh1 in https://github.com/pydantic/pydantic/pull/11321
* Add additional allowed schemes for `ClickHouseDsn` by @Maze21127 in https://github.com/pydantic/pydantic/pull/11319
* Coerce decimal constraints to `Decimal` instances by @Viicos in https://github.com/pydantic/pydantic/pull/11350
* Use the correct JSON Schema mode when handling function schemas by @Viicos in https://github.com/pydantic/pydantic/pull/11367
* Improve exception message when encountering recursion errors during type evaluation by @Viicos in https://github.com/pydantic/pydantic/pull/11356
* Always include `additionalProperties: True` for arbitrary dictionary schemas by @austinyu in https://github.com/pydantic/pydantic/pull/11392
* Expose `fallback` parameter in serialization methods by @Viicos in https://github.com/pydantic/pydantic/pull/11398
* Fix path serialization behavior by @sydney-runkle in https://github.com/pydantic/pydantic/pull/11416
* Do not reuse validators and serializers during model rebuild by @Viicos in https://github.com/pydantic/pydantic/pull/11429
* Collect model fields when rebuilding a model by @Viicos in https://github.com/pydantic/pydantic/pull/11388
* Allow cached properties to be altered on frozen models by @Viicos in https://github.com/pydantic/pydantic/pull/11432
* Fix tuple serialization for `Sequence` types by @sydney-runkle in https://github.com/pydantic/pydantic/pull/11435
* Fix: do not check for `__get_validators__` on classes where `__get_pydantic_core_schema__` is also defined by @tlambert03 in https://github.com/pydantic/pydantic/pull/11444
* Allow callable instances to be used as serializers by @Viicos in https://github.com/pydantic/pydantic/pull/11451
* Improve error thrown when overriding field with a property by @sydney-runkle in https://github.com/pydantic/pydantic/pull/11459
* Fix JSON Schema generation with referenceable core schemas holding JSON metadata by @Viicos in https://github.com/pydantic/pydantic/pull/11475
* Support strict specification on union member types by @sydney-runkle in https://github.com/pydantic/pydantic/pull/11481
* Implicitly set `validate_by_name` to `True` when `validate_by_alias` is `False` by @sydney-runkle in https://github.com/pydantic/pydantic/pull/11503
* Change type of `Any` when synthesizing `BaseSettings.__init__` signature in the mypy plugin by @Viicos in https://github.com/pydantic/pydantic/pull/11497
* Support type variable defaults referencing other type variables by @Viicos in https://github.com/pydantic/pydantic/pull/11520
* Fix `ValueError` on year zero by @davidhewitt in https://github.com/pydantic/pydantic-core/pull/1583
* `dataclass` `InitVar` shouldn't be required on serialization by @sydney-runkle in https://github.com/pydantic/pydantic-core/pull/1602

## New Contributors

* @FyZzyss made their first contribution in https://github.com/pydantic/pydantic/pull/10789
* @tamird made their first contribution in https://github.com/pydantic/pydantic/pull/10948
* @felixxm made their first contribution in https://github.com/pydantic/pydantic/pull/11077
* @alexprabhat99 made their first contribution in https://github.com/pydantic/pydantic/pull/11082
* @Kharianne made their first contribution in https://github.com/pydantic/pydantic/pull/11111
* @mdaffad made their first contribution in https://github.com/pydantic/pydantic/pull/11177
* @thejcannon made their first contribution in https://github.com/pydantic/pydantic/pull/11014
* @thomasfrimannkoren made their first contribution in https://github.com/pydantic/pydantic/pull/11251
* @usernameMAI made their first contribution in https://github.com/pydantic/pydantic/pull/11275
* @ananiavito made their first contribution in https://github.com/pydantic/pydantic/pull/11302
* @pawamoy made their first contribution in https://github.com/pydantic/pydantic/pull/11311
* @Maze21127 made their first contribution in https://github.com/pydantic/pydantic/pull/11319
* @kauabh made their first contribution in https://github.com/pydantic/pydantic/pull/11369
* @jaceklaskowski made their first contribution in https://github.com/pydantic/pydantic/pull/11353
* @tmpbeing made their first contribution in https://github.com/pydantic/pydantic/pull/11375
* @petyosi made their first contribution in https://github.com/pydantic/pydantic/pull/11405
* @austinyu made their first contribution in https://github.com/pydantic/pydantic/pull/11392
* @mikeedjones made their first contribution in https://github.com/pydantic/pydantic/pull/11402
* @astei made their first contribution in https://github.com/pydantic/pydantic/pull/11436
* @dsayling made their first contribution in https://github.com/pydantic/pydantic/pull/11522
* @sobolevn made their first contribution in https://github.com/pydantic/pydantic-core/pull/1645

## v2.11.0a2 (2025-02-10)

[GitHub release](https://github.com/pydantic/pydantic/releases/tag/v2.11.0a2)

### What's Changed

Pydantic v2.11 is a version strongly focused on build time performance of Pydantic models (and core schema generation in general).
This is another early alpha release, meant to collect early feedback from users having issues with core schema builds.

#### Packaging

* Bump `ruff` from 0.9.2 to 0.9.5 by @Viicos in [#11407](https://github.com/pydantic/pydantic/pull/11407)
* Bump `pydantic-core` to v2.29.0 by @mikeedjones in [#11402](https://github.com/pydantic/pydantic/pull/11402)
* Use locally-built rust with symbols & pgo by @davidhewitt in [#11403](https://github.com/pydantic/pydantic/pull/11403)

#### Performance

* Create a single dictionary when creating a `CoreConfig` instance by @sydney-runkle in [#11384](https://github.com/pydantic/pydantic/pull/11384)

#### Fixes

* Use the correct JSON Schema mode when handling function schemas by @Viicos in [#11367](https://github.com/pydantic/pydantic/pull/11367)
* Fix JSON Schema reference logic with `examples` keys by @Viicos in [#11366](https://github.com/pydantic/pydantic/pull/11366)
* Improve exception message when encountering recursion errors during type evaluation by @Viicos in [#11356](https://github.com/pydantic/pydantic/pull/11356)
* Always include `additionalProperties: True` for arbitrary dictionary schemas by @austinyu in [#11392](https://github.com/pydantic/pydantic/pull/11392)
* Expose `fallback` parameter in serialization methods by @Viicos in [#11398](https://github.com/pydantic/pydantic/pull/11398)
* Fix path serialization behavior by @sydney-runkle in [#11416](https://github.com/pydantic/pydantic/pull/11416)

### New Contributors

* @kauabh made their first contribution in [#11369](https://github.com/pydantic/pydantic/pull/11369)
* @jaceklaskowski made their first contribution in [#11353](https://github.com/pydantic/pydantic/pull/11353)
* @tmpbeing made their first contribution in [#11375](https://github.com/pydantic/pydantic/pull/11375)
* @petyosi made their first contribution in [#11405](https://github.com/pydantic/pydantic/pull/11405)
* @austinyu made their first contribution in [#11392](https://github.com/pydantic/pydantic/pull/11392)
* @mikeedjones made their first contribution in [#11402](https://github.com/pydantic/pydantic/pull/11402)

## v2.11.0a1 (2025-01-30)

[GitHub release](https://github.com/pydantic/pydantic/releases/tag/v2.11.0a1)

### What's Changed

Pydantic v2.11 is a version strongly focused on build time performance of Pydantic models (and core schema generation in general).
This is an early alpha release, meant to collect early feedback from users having issues with core schema builds.

#### Packaging

* Bump dawidd6/action-download-artifact from 6 to 7 by @dependabot in [#11018](https://github.com/pydantic/pydantic/pull/11018)
* Re-enable memray related tests on Python 3.12+ by @Viicos in [#11191](https://github.com/pydantic/pydantic/pull/11191)
* Bump astral-sh/setup-uv to 5 by @dependabot in [#11205](https://github.com/pydantic/pydantic/pull/11205)
* Bump `ruff` to v0.9.0 by @sydney-runkle in [#11254](https://github.com/pydantic/pydantic/pull/11254)
* Regular `uv.lock` deps update by @sydney-runkle in [#11333](https://github.com/pydantic/pydantic/pull/11333)
* Add a `check_pydantic_core_version()` function by @Viicos in [#11324](https://github.com/pydantic/pydantic/pull/11324)
* Remove `greenlet` development dependency by @Viicos in [#11351](https://github.com/pydantic/pydantic/pull/11351)
* Bump `pydantic-core` to v2.28.0 by @Viicos in [#11364](https://github.com/pydantic/pydantic/pull/11364)

#### New Features

* Support unsubstituted type variables with both a default and a bound or constraints by @FyZzyss in [#10789](https://github.com/pydantic/pydantic/pull/10789)
* Add a `default_factory_takes_validated_data` property to `FieldInfo` by @Viicos in [#11034](https://github.com/pydantic/pydantic/pull/11034)
* Raise a better error when a generic alias is used inside `type[]` by @Viicos in [#11088](https://github.com/pydantic/pydantic/pull/11088)
* Properly support PEP 695 generics syntax by @Viicos in [#11189](https://github.com/pydantic/pydantic/pull/11189)
* Properly support type variable defaults by @Viicos in [#11332](https://github.com/pydantic/pydantic/pull/11332)

#### Changes

* Rework `create_model` field definitions format by @Viicos in [#11032](https://github.com/pydantic/pydantic/pull/11032)
* Raise a deprecation warning when a field is annotated as final with a default value by @Viicos in [#11168](https://github.com/pydantic/pydantic/pull/11168)
* Deprecate accessing `model_fields` and `model_computed_fields` on instances by @Viicos in [#11169](https://github.com/pydantic/pydantic/pull/11169)
* Move core schema generation logic for path types inside the `GenerateSchema` class by @sydney-runkle in [#10846](https://github.com/pydantic/pydantic/pull/10846)
* Move `deque` schema gen to `GenerateSchema` class by @sydney-runkle in [#11239](https://github.com/pydantic/pydantic/pull/11239)
* Move `Mapping` schema gen to `GenerateSchema` to complete removal of `prepare_annotations_for_known_type` workaround by @sydney-runkle in [#11247](https://github.com/pydantic/pydantic/pull/11247)
* Remove Python 3.8 Support by @sydney-runkle in [#11258](https://github.com/pydantic/pydantic/pull/11258)
* Disable `pydantic-core` core schema validation by @sydney-runkle in [#11271](https://github.com/pydantic/pydantic/pull/11271)

#### Performance

* Only evaluate `FieldInfo` annotations if required during schema building by @Viicos in [#10769](https://github.com/pydantic/pydantic/pull/10769)
* Optimize calls to `get_type_ref` by @Viicos in [#10863](https://github.com/pydantic/pydantic/pull/10863)
* Improve `__setattr__` performance of Pydantic models by caching setter functions by @MarkusSintonen in [#10868](https://github.com/pydantic/pydantic/pull/10868)
* Improve annotation application performance by @Viicos in [#11186](https://github.com/pydantic/pydantic/pull/11186)
* Improve performance of `_typing_extra` module by @Viicos in [#11255](https://github.com/pydantic/pydantic/pull/11255)
* Refactor and optimize schema cleaning logic by @Viicos and @MarkusSintonen in [#11244](https://github.com/pydantic/pydantic/pull/11244)

#### Fixes

* Add validation tests for `_internal/_validators.py` by @tkasuz in [#10763](https://github.com/pydantic/pydantic/pull/10763)
* Improve `TypeAdapter` instance repr by @sydney-runkle in [#10872](https://github.com/pydantic/pydantic/pull/10872)
* Revert "ci: use locally built pydantic-core with debug symbols by @sydney-runkle in [#10942](https://github.com/pydantic/pydantic/pull/10942)
* Re-enable all FastAPI tests by @tamird in [#10948](https://github.com/pydantic/pydantic/pull/10948)
* Fix typo in HISTORY.md. by @felixxm in [#11077](https://github.com/pydantic/pydantic/pull/11077)
* Infer final fields with a default value as class variables in the mypy plugin by @Viicos in [#11121](https://github.com/pydantic/pydantic/pull/11121)
* Recursively unpack `Literal` values if using PEP 695 type aliases by @Viicos in [#11114](https://github.com/pydantic/pydantic/pull/11114)
* Override `__subclasscheck__` on `ModelMetaclass` to avoid memory leak and performance issues by @Viicos in [#11116](https://github.com/pydantic/pydantic/pull/11116)
* Remove unused `_extract_get_pydantic_json_schema()` parameter by @Viicos in [#11155](https://github.com/pydantic/pydantic/pull/11155)
* Add FastAPI and SQLModel to third-party tests by @sydney-runkle in [#11044](https://github.com/pydantic/pydantic/pull/11044)
* Fix conditional expressions syntax for third-party tests by @Viicos in [#11162](https://github.com/pydantic/pydantic/pull/11162)
* Move FastAPI tests to third-party workflow by @Viicos in [#11164](https://github.com/pydantic/pydantic/pull/11164)
* Improve discriminated union error message for invalid union variants by @Viicos in [#11161](https://github.com/pydantic/pydantic/pull/11161)
* Unpack PEP 695 type aliases if using the `Annotated` form by @Viicos in [#11109](https://github.com/pydantic/pydantic/pull/11109)
* Include `openapi-python-client` check in issue creation for third-party failures, use `main` branch by @sydney-runkle in [#11182](https://github.com/pydantic/pydantic/pull/11182)
* Add pandera third-party tests by @Viicos in [#11193](https://github.com/pydantic/pydantic/pull/11193)
* Add ODMantic third-party tests by @sydney-runkle in [#11197](https://github.com/pydantic/pydantic/pull/11197)
* Add missing stacklevel in `deprecated_instance_property` warning by @Viicos in [#11200](https://github.com/pydantic/pydantic/pull/11200)
* Copy `WithJsonSchema` schema to avoid sharing mutated data by @thejcannon in [#11014](https://github.com/pydantic/pydantic/pull/11014)
* Do not cache parametrized models when in the process of parametrizing another model by @Viicos in [#10704](https://github.com/pydantic/pydantic/pull/10704)
* Re-enable Beanie third-party tests by @Viicos in [#11214](https://github.com/pydantic/pydantic/pull/11214)
* Add discriminated union related metadata entries to the `CoreMetadata` definition by @Viicos in [#11216](https://github.com/pydantic/pydantic/pull/11216)
* Consolidate schema definitions logic in the `_Definitions` class by @Viicos in [#11208](https://github.com/pydantic/pydantic/pull/11208)
* Support initializing root model fields with values of the `root` type in the mypy plugin by @Viicos in [#11212](https://github.com/pydantic/pydantic/pull/11212)
* Fix various issues with dataclasses and `use_attribute_docstrings` by @Viicos in [#11246](https://github.com/pydantic/pydantic/pull/11246)
* Only compute normalized decimal places if necessary in `decimal_places_validator` by @misrasaurabh1 in [#11281](https://github.com/pydantic/pydantic/pull/11281)
* Fix two misplaced sentences in validation errors documentation by @ananiavito in [#11302](https://github.com/pydantic/pydantic/pull/11302)
* Fix mkdocstrings inventory example in documentation by @pawamoy in [#11311](https://github.com/pydantic/pydantic/pull/11311)
* Add support for `validation_alias` in the mypy plugin by @Viicos in [#11295](https://github.com/pydantic/pydantic/pull/11295)
* Do not transform model serializer functions as class methods in the mypy plugin by @Viicos in [#11298](https://github.com/pydantic/pydantic/pull/11298)
* Simplify `GenerateJsonSchema.literal_schema()` implementation by @misrasaurabh1 in [#11321](https://github.com/pydantic/pydantic/pull/11321)
* Add additional allowed schemes for `ClickHouseDsn` by @Maze21127 in [#11319](https://github.com/pydantic/pydantic/pull/11319)
* Coerce decimal constraints to `Decimal` instances by @Viicos in [#11350](https://github.com/pydantic/pydantic/pull/11350)
* Fix `ValueError` on year zero by @davidhewitt in [pydantic-core#1583](https://github.com/pydantic/pydantic-core/pull/1583)

### New Contributors

* @FyZzyss made their first contribution in [#10789](https://github.com/pydantic/pydantic/pull/10789)
* @tamird made their first contribution in [#10948](https://github.com/pydantic/pydantic/pull/10948)
* @felixxm made their first contribution in [#11077](https://github.com/pydantic/pydantic/pull/11077)
* @alexprabhat99 made their first contribution in [#11082](https://github.com/pydantic/pydantic/pull/11082)
* @Kharianne made their first contribution in [#11111](https://github.com/pydantic/pydantic/pull/11111)
* @mdaffad made their first contribution in [#11177](https://github.com/pydantic/pydantic/pull/11177)
* @thejcannon made their first contribution in [#11014](https://github.com/pydantic/pydantic/pull/11014)
* @thomasfrimannkoren made their first contribution in [#11251](https://github.com/pydantic/pydantic/pull/11251)
* @usernameMAI made their first contribution in [#11275](https://github.com/pydantic/pydantic/pull/11275)
* @ananiavito made their first contribution in [#11302](https://github.com/pydantic/pydantic/pull/11302)
* @pawamoy made their first contribution in [#11311](https://github.com/pydantic/pydantic/pull/11311)
* @Maze21127 made their first contribution in [#11319](https://github.com/pydantic/pydantic/pull/11319)

## v2.10.6 (2025-01-23)

[GitHub release](https://github.com/pydantic/pydantic/releases/tag/v2.10.6)

### What's Changed

#### Fixes

* Fix JSON Schema reference collection with `'examples'` keys by @Viicos in [#11325](https://github.com/pydantic/pydantic/pull/11325)
* Fix url python serialization by @sydney-runkle in [#11331](https://github.com/pydantic/pydantic/pull/11331)

## v2.10.5 (2025-01-08)

[GitHub release](https://github.com/pydantic/pydantic/releases/tag/v2.10.5)

### What's Changed

#### Fixes

* Remove custom MRO implementation of Pydantic models by @Viicos in [#11184](https://github.com/pydantic/pydantic/pull/11184)
* Fix URL serialization for unions by @sydney-runkle in [#11233](https://github.com/pydantic/pydantic/pull/11233)

## v2.10.4 (2024-12-18)

[GitHub release](https://github.com/pydantic/pydantic/releases/tag/v2.10.4)

### What's Changed

#### Packaging

* Bump `pydantic-core` to v2.27.2 by @davidhewitt in [#11138](https://github.com/pydantic/pydantic/pull/11138)

#### Fixes

* Fix for comparison of `AnyUrl` objects by @alexprabhat99 in [#11082](https://github.com/pydantic/pydantic/pull/11082)
* Properly fetch PEP 695 type params for functions, do not fetch annotations from signature by @Viicos in [#11093](https://github.com/pydantic/pydantic/pull/11093)
* Include JSON Schema input core schema in function schemas by @Viicos in [#11085](https://github.com/pydantic/pydantic/pull/11085)
* Add `len` to `_BaseUrl` to avoid TypeError by @Kharianne in [#11111](https://github.com/pydantic/pydantic/pull/11111)
* Make sure the type reference is removed from the seen references by @Viicos in [#11143](https://github.com/pydantic/pydantic/pull/11143)

### New Contributors

* @FyZzyss made their first contribution in [#10789](https://github.com/pydantic/pydantic/pull/10789)
* @tamird made their first contribution in [#10948](https://github.com/pydantic/pydantic/pull/10948)
* @felixxm made their first contribution in [#11077](https://github.com/pydantic/pydantic/pull/11077)
* @alexprabhat99 made their first contribution in [#11082](https://github.com/pydantic/pydantic/pull/11082)
* @Kharianne made their first contribution in [#11111](https://github.com/pydantic/pydantic/pull/11111)

## v2.10.3 (2024-12-03)

[GitHub release](https://github.com/pydantic/pydantic/releases/tag/v2.10.3)

### What's Changed

#### Fixes

* Set fields when `defer_build` is set on Pydantic dataclasses by @Viicos in [#10984](https://github.com/pydantic/pydantic/pull/10984)
* Do not resolve the JSON Schema reference for `dict` core schema keys by @Viicos in [#10989](https://github.com/pydantic/pydantic/pull/10989)
* Use the globals of the function when evaluating the return type for `PlainSerializer` and `WrapSerializer` functions by @Viicos in [#11008](https://github.com/pydantic/pydantic/pull/11008)
* Fix host required enforcement for urls to be compatible with v2.9 behavior by @sydney-runkle in [#11027](https://github.com/pydantic/pydantic/pull/11027)
* Add a `default_factory_takes_validated_data` property to `FieldInfo` by @Viicos in [#11034](https://github.com/pydantic/pydantic/pull/11034)
* Fix url json schema in `serialization` mode by @sydney-runkle in [#11035](https://github.com/pydantic/pydantic/pull/11035)

## v2.10.2 (2024-11-25)

[GitHub release](https://github.com/pydantic/pydantic/releases/tag/v2.10.2)

### What's Changed

#### Fixes

* Only evaluate FieldInfo annotations if required during schema building by @Viicos in [#10769](https://github.com/pydantic/pydantic/pull/10769)
* Do not evaluate annotations for private fields by @Viicos in [#10962](https://github.com/pydantic/pydantic/pull/10962)
* Support serialization as any for `Secret` types and `Url` types by @sydney-runkle in [#10947](https://github.com/pydantic/pydantic/pull/10947)
* Fix type hint of `Field.default` to be compatible with Python 3.8 and 3.9 by @Viicos in [#10972](https://github.com/pydantic/pydantic/pull/10972)
* Add hashing support for URL types by @sydney-runkle in [#10975](https://github.com/pydantic/pydantic/pull/10975)
* Hide `BaseModel.__replace__` definition from type checkers by @Viicos in [#10979](https://github.com/pydantic/pydantic/pull/10979)

## v2.10.1 (2024-11-21)

[GitHub release](https://github.com/pydantic/pydantic/releases/tag/v2.10.1)

### What's Changed

#### Packaging

* Bump `pydantic-core` version to `v2.27.1` by @sydney-runkle in [#10938](https://github.com/pydantic/pydantic/pull/10938)

#### Fixes

* Use the correct frame when instantiating a parametrized `TypeAdapter` by @Viicos in [#10893](https://github.com/pydantic/pydantic/pull/10893)
* Relax check for validated data in `default_factory` utils by @sydney-runkle in [#10909](https://github.com/pydantic/pydantic/pull/10909)
* Fix type checking issue with `model_fields` and `model_computed_fields` by @sydney-runkle in [#10911](https://github.com/pydantic/pydantic/pull/10911)
* Use the parent configuration during schema generation for stdlib `dataclass`es by @sydney-runkle in [#10928](https://github.com/pydantic/pydantic/pull/10928)
* Use the `globals` of the function when evaluating the return type of serializers and `computed_field`s by @Viicos in [#10929](https://github.com/pydantic/pydantic/pull/10929)
* Fix URL constraint application by @sydney-runkle in [#10922](https://github.com/pydantic/pydantic/pull/10922)
* Fix URL equality with different validation methods by @sydney-runkle in [#10934](https://github.com/pydantic/pydantic/pull/10934)
* Fix JSON schema title when specified as `''` by @sydney-runkle in [#10936](https://github.com/pydantic/pydantic/pull/10936)
* Fix `python` mode serialization for `complex` inference by @sydney-runkle in [pydantic-core#1549](https://github.com/pydantic/pydantic-core/pull/1549)

### New Contributors

## v2.10.0 (2024-11-20)

The code released in v2.10.0 is practically identical to that of v2.10.0b2.

[GitHub release](https://github.com/pydantic/pydantic/releases/tag/v2.10.0)

See the [v2.10 release blog post](https://pydantic.dev/articles/pydantic-v2-10-release) for the highlights!

### What's Changed

#### Packaging

* Bump `pydantic-core` to `v2.27.0` by @sydney-runkle in [#10825](https://github.com/pydantic/pydantic/pull/10825)
* Replaced pdm with uv by @frfahim in [#10727](https://github.com/pydantic/pydantic/pull/10727)

#### New Features

* Support `fractions.Fraction` by @sydney-runkle in [#10318](https://github.com/pydantic/pydantic/pull/10318)
* Support `Hashable` for json validation by @sydney-runkle in [#10324](https://github.com/pydantic/pydantic/pull/10324)
* Add a `SocketPath` type for `linux` systems by @theunkn0wn1 in [#10378](https://github.com/pydantic/pydantic/pull/10378)
* Allow arbitrary refs in JSON schema `examples` by @sydney-runkle in [#10417](https://github.com/pydantic/pydantic/pull/10417)
* Support `defer_build` for Pydantic dataclasses by @Viicos in [#10313](https://github.com/pydantic/pydantic/pull/10313)
* Adding v1 / v2 incompatibility warning for nested v1 model by @sydney-runkle in [#10431](https://github.com/pydantic/pydantic/pull/10431)
* Add support for unpacked `TypedDict` to type hint variadic keyword arguments with `@validate_call` by @Viicos in [#10416](https://github.com/pydantic/pydantic/pull/10416)
* Support compiled patterns in `protected_namespaces` by @sydney-runkle in [#10522](https://github.com/pydantic/pydantic/pull/10522)
* Add support for `propertyNames` in JSON schema by @FlorianSW in [#10478](https://github.com/pydantic/pydantic/pull/10478)
* Adding `__replace__` protocol for Python 3.13+ support by @sydney-runkle in [#10596](https://github.com/pydantic/pydantic/pull/10596)
* Expose public `sort` method for JSON schema generation by @sydney-runkle in [#10595](https://github.com/pydantic/pydantic/pull/10595)
* Add runtime validation of `@validate_call` callable argument by @kc0506 in [#10627](https://github.com/pydantic/pydantic/pull/10627)
* Add `experimental_allow_partial` support by @samuelcolvin in [#10748](https://github.com/pydantic/pydantic/pull/10748)
* Support default factories taking validated data as an argument by @Viicos in [#10678](https://github.com/pydantic/pydantic/pull/10678)
* Allow subclassing `ValidationError` and `PydanticCustomError` by @Youssefares in [pydantic/pydantic-core#1413](https://github.com/pydantic/pydantic-core/pull/1413)
* Add `trailing-strings` support to `experimental_allow_partial` by @sydney-runkle in [#10825](https://github.com/pydantic/pydantic/pull/10825)
* Add `rebuild()` method for `TypeAdapter` and simplify `defer_build` patterns by @sydney-runkle in [#10537](https://github.com/pydantic/pydantic/pull/10537)
* Improve `TypeAdapter` instance repr by @sydney-runkle in [#10872](https://github.com/pydantic/pydantic/pull/10872)

#### Changes

* Don't allow customization of `SchemaGenerator` until interface is more stable by @sydney-runkle in [#10303](https://github.com/pydantic/pydantic/pull/10303)
* Cleanly `defer_build` on `TypeAdapters`, removing experimental flag by @sydney-runkle in [#10329](https://github.com/pydantic/pydantic/pull/10329)
* Fix `mro` of generic subclass  by @kc0506 in [#10100](https://github.com/pydantic/pydantic/pull/10100)
* Strip whitespaces on JSON Schema title generation by @sydney-runkle in [#10404](https://github.com/pydantic/pydantic/pull/10404)
* Use `b64decode` and `b64encode` for `Base64Bytes` type by @sydney-runkle in [#10486](https://github.com/pydantic/pydantic/pull/10486)
* Relax protected namespace config default by @sydney-runkle in [#10441](https://github.com/pydantic/pydantic/pull/10441)
* Revalidate parametrized generics if instance's origin is subclass of OG class by @sydney-runkle in [#10666](https://github.com/pydantic/pydantic/pull/10666)
* Warn if configuration is specified on the `@dataclass` decorator and with the `__pydantic_config__` attribute by @sydney-runkle in [#10406](https://github.com/pydantic/pydantic/pull/10406)
* Recommend against using `Ellipsis` (...) with `Field` by @Viicos in [#10661](https://github.com/pydantic/pydantic/pull/10661)
* Migrate to subclassing instead of annotated approach for pydantic url types by @sydney-runkle in [#10662](https://github.com/pydantic/pydantic/pull/10662)
* Change JSON schema generation of `Literal`s and `Enums` by @Viicos in [#10692](https://github.com/pydantic/pydantic/pull/10692)
* Simplify unions involving `Any` or `Never` when replacing type variables by @Viicos in [#10338](https://github.com/pydantic/pydantic/pull/10338)
* Do not require padding when decoding `base64` bytes by @bschoenmaeckers in [pydantic/pydantic-core#1448](https://github.com/pydantic/pydantic-core/pull/1448)
* Support dates all the way to 1BC by @changhc in [pydantic/speedate#77](https://github.com/pydantic/speedate/pull/77)

#### Performance

* Schema cleaning: skip unnecessary copies during schema walking by @Viicos in [#10286](https://github.com/pydantic/pydantic/pull/10286)
* Refactor namespace logic for annotations evaluation by @Viicos in [#10530](https://github.com/pydantic/pydantic/pull/10530)
* Improve email regexp on edge cases by @AlekseyLobanov in [#10601](https://github.com/pydantic/pydantic/pull/10601)
* `CoreMetadata` refactor with an emphasis on documentation, schema build time performance, and reducing complexity by @sydney-runkle in [#10675](https://github.com/pydantic/pydantic/pull/10675)

#### Fixes

* Remove guarding check on `computed_field` with `field_serializer` by @nix010 in [#10390](https://github.com/pydantic/pydantic/pull/10390)
* Fix `Predicate` issue in `v2.9.0` by @sydney-runkle in [#10321](https://github.com/pydantic/pydantic/pull/10321)
* Fixing `annotated-types` bound by @sydney-runkle in [#10327](https://github.com/pydantic/pydantic/pull/10327)
* Turn `tzdata` install requirement into optional `timezone` dependency by @jakob-keller in [#10331](https://github.com/pydantic/pydantic/pull/10331)
* Use correct types namespace when building `namedtuple` core schemas by @Viicos in [#10337](https://github.com/pydantic/pydantic/pull/10337)
* Fix evaluation of stringified annotations during namespace inspection by @Viicos in [#10347](https://github.com/pydantic/pydantic/pull/10347)
* Fix `IncEx` type alias definition by @Viicos in [#10339](https://github.com/pydantic/pydantic/pull/10339)
* Do not error when trying to evaluate annotations of private attributes by @Viicos in [#10358](https://github.com/pydantic/pydantic/pull/10358)
* Fix nested type statement by @kc0506 in [#10369](https://github.com/pydantic/pydantic/pull/10369)
* Improve typing of `ModelMetaclass.mro` by @Viicos in [#10372](https://github.com/pydantic/pydantic/pull/10372)
* Fix class access of deprecated `computed_field`s by @Viicos in [#10391](https://github.com/pydantic/pydantic/pull/10391)
* Make sure `inspect.iscoroutinefunction` works on coroutines decorated with `@validate_call` by @MovisLi in [#10374](https://github.com/pydantic/pydantic/pull/10374)
* Fix `NameError` when using `validate_call` with PEP 695 on a class by @kc0506 in [#10380](https://github.com/pydantic/pydantic/pull/10380)
* Fix `ZoneInfo` with various invalid types by @sydney-runkle in [#10408](https://github.com/pydantic/pydantic/pull/10408)
* Fix `PydanticUserError` on empty `model_config` with annotations by @cdwilson in [#10412](https://github.com/pydantic/pydantic/pull/10412)
* Fix variance issue in `_IncEx` type alias, only allow `True` by @Viicos in [#10414](https://github.com/pydantic/pydantic/pull/10414)
* Fix serialization schema generation when using `PlainValidator` by @Viicos in [#10427](https://github.com/pydantic/pydantic/pull/10427)
* Fix schema generation error when serialization schema holds references by @Viicos in [#10444](https://github.com/pydantic/pydantic/pull/10444)
* Inline references if possible when generating schema for `json_schema_input_type` by @Viicos in [#10439](https://github.com/pydantic/pydantic/pull/10439)
* Fix recursive arguments in `Representation` by @Viicos in [#10480](https://github.com/pydantic/pydantic/pull/10480)
* Fix representation for builtin function types by @kschwab in [#10479](https://github.com/pydantic/pydantic/pull/10479)
* Add python validators for decimal constraints (`max_digits` and `decimal_places`) by @sydney-runkle in [#10506](https://github.com/pydantic/pydantic/pull/10506)
* Only fetch `__pydantic_core_schema__` from the current class during schema generation by @Viicos in [#10518](https://github.com/pydantic/pydantic/pull/10518)
* Fix `stacklevel` on deprecation warnings for `BaseModel` by @sydney-runkle in [#10520](https://github.com/pydantic/pydantic/pull/10520)
* Fix warning `stacklevel` in `BaseModel.__init__` by @Viicos in [#10526](https://github.com/pydantic/pydantic/pull/10526)
* Improve error handling for in-evaluable refs for discriminator application by @sydney-runkle in [#10440](https://github.com/pydantic/pydantic/pull/10440)
* Change the signature of `ConfigWrapper.core_config` to take the title directly by @Viicos in [#10562](https://github.com/pydantic/pydantic/pull/10562)
* Do not use the previous config from the stack for dataclasses without config by @Viicos in [#10576](https://github.com/pydantic/pydantic/pull/10576)
* Fix serialization for IP types with `mode='python'` by @sydney-runkle in [#10594](https://github.com/pydantic/pydantic/pull/10594)
* Support constraint application for `Base64Etc` types by @sydney-runkle in [#10584](https://github.com/pydantic/pydantic/pull/10584)
* Fix `validate_call` ignoring `Field` in `Annotated` by @kc0506 in [#10610](https://github.com/pydantic/pydantic/pull/10610)
* Raise an error when `Self` is invalid by @kc0506 in [#10609](https://github.com/pydantic/pydantic/pull/10609)
* Using `core_schema.InvalidSchema` instead of metadata injection + checks by @sydney-runkle in [#10523](https://github.com/pydantic/pydantic/pull/10523)
* Tweak type alias logic by @kc0506 in [#10643](https://github.com/pydantic/pydantic/pull/10643)
* Support usage of `type` with `typing.Self` and type aliases by @kc0506 in [#10621](https://github.com/pydantic/pydantic/pull/10621)
* Use overloads for `Field` and `PrivateAttr` functions by @Viicos in [#10651](https://github.com/pydantic/pydantic/pull/10651)
* Clean up the `mypy` plugin implementation by @Viicos in [#10669](https://github.com/pydantic/pydantic/pull/10669)
* Properly check for `typing_extensions` variant of `TypeAliasType` by @Daraan in [#10713](https://github.com/pydantic/pydantic/pull/10713)
* Allow any mapping in `BaseModel.model_copy()` by @Viicos in [#10751](https://github.com/pydantic/pydantic/pull/10751)
* Fix `isinstance` behavior for urls by @sydney-runkle in [#10766](https://github.com/pydantic/pydantic/pull/10766)
* Ensure `cached_property` can be set on Pydantic models by @Viicos in [#10774](https://github.com/pydantic/pydantic/pull/10774)
* Fix equality checks for primitives in literals by @sydney-runkle in [pydantic/pydantic-core#1459](https://github.com/pydantic/pydantic-core/pull/1459)
* Properly enforce `host_required` for URLs by @Viicos in [pydantic/pydantic-core#1488](https://github.com/pydantic/pydantic-core/pull/1488)
* Fix when `coerce_numbers_to_str` enabled and string has invalid Unicode character by @andrey-berenda in [pydantic/pydantic-core#1515](https://github.com/pydantic/pydantic-core/pull/1515)
* Fix serializing `complex` values in `Enum`s by @changhc in [pydantic/pydantic-core#1524](https://github.com/pydantic/pydantic-core/pull/1524)
* Refactor `_typing_extra` module by @Viicos in [#10725](https://github.com/pydantic/pydantic/pull/10725)
* Support intuitive equality for urls by @sydney-runkle in [#10798](https://github.com/pydantic/pydantic/pull/10798)
* Add `bytearray` to `TypeAdapter.validate_json` signature by @samuelcolvin in [#10802](https://github.com/pydantic/pydantic/pull/10802)
* Ensure class access of method descriptors is performed when used as a default with `Field` by @Viicos in [#10816](https://github.com/pydantic/pydantic/pull/10816)
* Fix circular import with `validate_call` by @sydney-runkle in [#10807](https://github.com/pydantic/pydantic/pull/10807)
* Fix error when using type aliases referencing other type aliases by @Viicos in [#10809](https://github.com/pydantic/pydantic/pull/10809)
* Fix `IncEx` type alias to be compatible with mypy by @Viicos in [#10813](https://github.com/pydantic/pydantic/pull/10813)
* Make `__signature__` a lazy property, do not deepcopy defaults by @Viicos in [#10818](https://github.com/pydantic/pydantic/pull/10818)
* Make `__signature__` lazy for dataclasses, too by @sydney-runkle in [#10832](https://github.com/pydantic/pydantic/pull/10832)
* Subclass all single host url classes from `AnyUrl` to preserve behavior from v2.9 by @sydney-runkle in [#10856](https://github.com/pydantic/pydantic/pull/10856)

### New Contributors

* @jakob-keller made their first contribution in [#10331](https://github.com/pydantic/pydantic/pull/10331)
* @MovisLi made their first contribution in [#10374](https://github.com/pydantic/pydantic/pull/10374)
* @joaopalmeiro made their first contribution in [#10405](https://github.com/pydantic/pydantic/pull/10405)
* @theunkn0wn1 made their first contribution in [#10378](https://github.com/pydantic/pydantic/pull/10378)
* @cdwilson made their first contribution in [#10412](https://github.com/pydantic/pydantic/pull/10412)
* @dlax made their first contribution in [#10421](https://github.com/pydantic/pydantic/pull/10421)
* @kschwab made their first contribution in [#10479](https://github.com/pydantic/pydantic/pull/10479)
* @santibreo made their first contribution in [#10453](https://github.com/pydantic/pydantic/pull/10453)
* @FlorianSW made their first contribution in [#10478](https://github.com/pydantic/pydantic/pull/10478)
* @tkasuz made their first contribution in [#10555](https://github.com/pydantic/pydantic/pull/10555)
* @AlekseyLobanov made their first contribution in [#10601](https://github.com/pydantic/pydantic/pull/10601)
* @NiclasvanEyk made their first contribution in [#10667](https://github.com/pydantic/pydantic/pull/10667)
* @mschoettle made their first contribution in [#10677](https://github.com/pydantic/pydantic/pull/10677)
* @Daraan made their first contribution in [#10713](https://github.com/pydantic/pydantic/pull/10713)
* @k4nar made their first contribution in [#10736](https://github.com/pydantic/pydantic/pull/10736)
* @UriyaHarpeness made their first contribution in [#10740](https://github.com/pydantic/pydantic/pull/10740)
* @frfahim made their first contribution in [#10727](https://github.com/pydantic/pydantic/pull/10727)

## v2.10.0b2 (2024-11-13)

Pre-release, see [the GitHub release](https://github.com/pydantic/pydantic/releases/tag/v2.10.0b2) for details.

## v2.10.0b1 (2024-11-06)

Pre-release, see [the GitHub release](https://github.com/pydantic/pydantic/releases/tag/v2.10.0b1) for details.

<!-- package description limit -->

## v2.9.2 (2024-09-17)

[GitHub release](https://github.com/pydantic/pydantic/releases/tag/v2.9.2)

### What's Changed

#### Fixes

* Do not error when trying to evaluate annotations of private attributes by @Viicos in [#10358](https://github.com/pydantic/pydantic/pull/10358)
* Adding notes on designing sound `Callable` discriminators by @sydney-runkle in [#10400](https://github.com/pydantic/pydantic/pull/10400)
* Fix serialization schema generation when using `PlainValidator` by @Viicos in [#10427](https://github.com/pydantic/pydantic/pull/10427)
* Fix `Union` serialization warnings by @sydney-runkle in [pydantic/pydantic-core#1449](https://github.com/pydantic/pydantic-core/pull/1449)
* Fix variance issue in `_IncEx` type alias, only allow `True` by @Viicos in [#10414](https://github.com/pydantic/pydantic/pull/10414)
* Fix `ZoneInfo` validation with various invalid types by @sydney-runkle in [#10408](https://github.com/pydantic/pydantic/pull/10408)

## v2.9.1 (2024-09-09)

[GitHub release](https://github.com/pydantic/pydantic/releases/tag/v2.9.1)

### What's Changed

#### Fixes

* Fix Predicate issue in v2.9.0 by @sydney-runkle in [#10321](https://github.com/pydantic/pydantic/pull/10321)
* Fixing `annotated-types` bound to `>=0.6.0` by @sydney-runkle in [#10327](https://github.com/pydantic/pydantic/pull/10327)
* Turn `tzdata` install requirement into optional `timezone` dependency by @jakob-keller in [#10331](https://github.com/pydantic/pydantic/pull/10331)
* Fix `IncExc` type alias definition by @Viicos in [#10339](https://github.com/pydantic/pydantic/pull/10339)
* Use correct types namespace when building namedtuple core schemas by @Viicos in [#10337](https://github.com/pydantic/pydantic/pull/10337)
* Fix evaluation of stringified annotations during namespace inspection by @Viicos in [#10347](https://github.com/pydantic/pydantic/pull/10347)
* Fix tagged union serialization with alias generators by @sydney-runkle in [pydantic/pydantic-core#1442](https://github.com/pydantic/pydantic-core/pull/1442)

## v2.9.0 (2024-09-05)

[GitHub release](https://github.com/pydantic/pydantic/releases/tag/v2.9.0)

The code released in v2.9.0 is practically identical to that of v2.9.0b2.

### What's Changed

#### Packaging

* Bump `ruff` to `v0.5.0` and `pyright` to `v1.1.369` by @sydney-runkle in [#9801](https://github.com/pydantic/pydantic/pull/9801)
* Bump `pydantic-extra-types` to `v2.9.0` by @sydney-runkle in [#9832](https://github.com/pydantic/pydantic/pull/9832)
* Support compatibility with `pdm v2.18.1` by @Viicos in [#10138](https://github.com/pydantic/pydantic/pull/10138)
* Bump `v1` version stub to `v1.10.18` by @sydney-runkle in [#10214](https://github.com/pydantic/pydantic/pull/10214)
* Bump `pydantic-core` to `v2.23.2` by @sydney-runkle in [#10311](https://github.com/pydantic/pydantic/pull/10311)

#### New Features

* Add support for `ZoneInfo` by @Youssefares in [#9896](https://github.com/pydantic/pydantic/pull/9896)
* Add `Config.val_json_bytes` by @josh-newman in [#9770](https://github.com/pydantic/pydantic/pull/9770)
* Add DSN for Snowflake by @aditkumar72 in [#10128](https://github.com/pydantic/pydantic/pull/10128)
* Support `complex` number by @changhc in [#9654](https://github.com/pydantic/pydantic/pull/9654)
* Add support for `annotated_types.Not` by @aditkumar72 in [#10210](https://github.com/pydantic/pydantic/pull/10210)
* Allow `WithJsonSchema` to inject `$ref`s w/ `http` or `https` links by @dAIsySHEng1 in [#9863](https://github.com/pydantic/pydantic/pull/9863)
* Allow validators to customize validation JSON schema by @Viicos in [#10094](https://github.com/pydantic/pydantic/pull/10094)
* Support parametrized `PathLike` types by @nix010 in [#9764](https://github.com/pydantic/pydantic/pull/9764)
* Add tagged union serializer that attempts to use `str` or `callable` discriminators to select the correct serializer by @sydney-runkle in in [pydantic/pydantic-core#1397](https://github.com/pydantic/pydantic-core/pull/1397)

#### Changes

* Breaking Change: Merge `dict` type `json_schema_extra` by @sydney-runkle in [#9792](https://github.com/pydantic/pydantic/pull/9792)
    * For more info (how to replicate old behavior) on this change, see [here](https://docs.pydantic.dev/dev/concepts/json_schema/#merging-json_schema_extra)
* Refactor annotation injection for known (often generic) types by @sydney-runkle in [#9979](https://github.com/pydantic/pydantic/pull/9979)
* Move annotation compatibility errors to validation phase by @sydney-runkle in [#9999](https://github.com/pydantic/pydantic/pull/9999)
* Improve runtime errors for string constraints like `pattern` for incompatible types by @sydney-runkle in [#10158](https://github.com/pydantic/pydantic/pull/10158)
* Remove `'allOf'` JSON schema workarounds by @dpeachey in [#10029](https://github.com/pydantic/pydantic/pull/10029)
* Remove `typed_dict_cls` data from `CoreMetadata` by @sydney-runkle in [#10180](https://github.com/pydantic/pydantic/pull/10180)
* Deprecate passing a dict to the `Examples` class by @Viicos in [#10181](https://github.com/pydantic/pydantic/pull/10181)
* Remove `initial_metadata` from internal metadata construct by @sydney-runkle in [#10194](https://github.com/pydantic/pydantic/pull/10194)
* Use `re.Pattern.search` instead of `re.Pattern.match` for consistency with `rust` behavior by @tinez in [pydantic/pydantic-core#1368](https://github.com/pydantic/pydantic-core/pull/1368)
* Show value of wrongly typed data in `pydantic-core` serialization warning by @BoxyUwU in [pydantic/pydantic-core#1377](https://github.com/pydantic/pydantic-core/pull/1377)
* Breaking Change: in `pydantic-core`, change `metadata` type hint in core schemas from `Any` -> `Dict[str, Any] | None` by @sydney-runkle in [pydantic/pydantic-core#1411](https://github.com/pydantic/pydantic-core/pull/1411)
* Raise helpful warning when `self` isn't returned from model validator by @sydney-runkle in [#10255](https://github.com/pydantic/pydantic/pull/10255)

#### Performance

* Initial start at improving import times for modules, using caching primarily by @sydney-runkle in [#10009](https://github.com/pydantic/pydantic/pull/10009)
* Using cached internal import for `BaseModel` by @sydney-runkle in [#10013](https://github.com/pydantic/pydantic/pull/10013)
* Simplify internal generics logic - remove generator overhead by @sydney-runkle in [#10059](https://github.com/pydantic/pydantic/pull/10059)
* Remove default module globals from types namespace by @sydney-runkle in [#10123](https://github.com/pydantic/pydantic/pull/10123)
* Performance boost: skip caching parent namespaces in most cases by @sydney-runkle in [#10113](https://github.com/pydantic/pydantic/pull/10113)
* Update ns stack with already copied ns by @sydney-runkle in [#10267](https://github.com/pydantic/pydantic/pull/10267)

##### Minor Internal Improvements

* ⚡️ Speed up `multiple_of_validator()` by 31% in `pydantic/_internal/_validators.py` by @misrasaurabh1 in [#9839](https://github.com/pydantic/pydantic/pull/9839)
* ⚡️ Speed up `ModelPrivateAttr.__set_name__()` by 18% in `pydantic/fields.py` by @misrasaurabh1 in [#9841](https://github.com/pydantic/pydantic/pull/9841)
* ⚡️ Speed up `dataclass()` by 7% in `pydantic/dataclasses.py` by @misrasaurabh1 in [#9843](https://github.com/pydantic/pydantic/pull/9843)
* ⚡️ Speed up function `_field_name_for_signature` by 37% in `pydantic/_internal/_signature.py` by @misrasaurabh1 in [#9951](https://github.com/pydantic/pydantic/pull/9951)
* ⚡️ Speed up method `GenerateSchema._unpack_refs_defs` by 26% in `pydantic/_internal/_generate_schema.py` by @misrasaurabh1 in [#9949](https://github.com/pydantic/pydantic/pull/9949)
* ⚡️ Speed up function `apply_each_item_validators` by 100% in `pydantic/_internal/_generate_schema.py` by @misrasaurabh1 in [#9950](https://github.com/pydantic/pydantic/pull/9950)
* ⚡️ Speed up method `ConfigWrapper.core_config` by 28% in `pydantic/_internal/_config.py` by @misrasaurabh1 in [#9953](https://github.com/pydantic/pydantic/pull/9953)

#### Fixes

* Respect `use_enum_values` on `Literal` types by @kwint in [#9787](https://github.com/pydantic/pydantic/pull/9787)
* Prevent type error for exotic `BaseModel/RootModel` inheritance by @dmontagu in [#9913](https://github.com/pydantic/pydantic/pull/9913)
* Fix typing issue with field_validator-decorated methods by @dmontagu in [#9914](https://github.com/pydantic/pydantic/pull/9914)
* Replace `str` type annotation with `Any` in validator factories in documentation on validators by @maximilianfellhuber in [#9885](https://github.com/pydantic/pydantic/pull/9885)
* Fix `ComputedFieldInfo.wrapped_property` pointer when a property setter is assigned by @tlambert03 in [#9892](https://github.com/pydantic/pydantic/pull/9892)
* Fix recursive typing of `main.IncEnx` by @tlambert03 in [#9924](https://github.com/pydantic/pydantic/pull/9924)
* Allow usage of `type[Annotated[...]]` by @Viicos in [#9932](https://github.com/pydantic/pydantic/pull/9932)
* `mypy` plugin: handle frozen fields on a per-field basis by @dmontagu in [#9935](https://github.com/pydantic/pydantic/pull/9935)
* Fix typo in `invalid-annotated-type` error code by @sydney-runkle in [#9948](https://github.com/pydantic/pydantic/pull/9948)
* Simplify schema generation for `uuid`, `url`, and `ip` types by @sydney-runkle in [#9975](https://github.com/pydantic/pydantic/pull/9975)
* Move `date` schemas to `_generate_schema.py` by @sydney-runkle in [#9976](https://github.com/pydantic/pydantic/pull/9976)
* Move `decimal.Decimal` validation to `_generate_schema.py` by @sydney-runkle in [#9977](https://github.com/pydantic/pydantic/pull/9977)
* Simplify IP address schema in `_std_types_schema.py` by @sydney-runkle in [#9959](https://github.com/pydantic/pydantic/pull/9959)
* Fix type annotations for some potentially generic `GenerateSchema.match_type` options by @sydney-runkle in [#9961](https://github.com/pydantic/pydantic/pull/9961)
* Add class name to "has conflict" warnings by @msabramo in [#9964](https://github.com/pydantic/pydantic/pull/9964)
* Fix `dataclass` ignoring `default_factory` passed in Annotated by @kc0506 in [#9971](https://github.com/pydantic/pydantic/pull/9971)
* Fix `Sequence` ignoring `discriminator` by @kc0506 in [#9980](https://github.com/pydantic/pydantic/pull/9980)
* Fix typing for `IPvAnyAddress` and `IPvAnyInterface` by @haoyun in [#9990](https://github.com/pydantic/pydantic/pull/9990)
* Fix false positives on v1 models in `mypy` plugin for `from_orm` check requiring from_attributes=True config by @radekwlsk in [#9938](https://github.com/pydantic/pydantic/pull/9938)
* Apply `strict=True` to `__init__` in `mypy` plugin by @kc0506 in [#9998](https://github.com/pydantic/pydantic/pull/9998)
* Refactor application of `deque` annotations by @sydney-runkle in [#10018](https://github.com/pydantic/pydantic/pull/10018)
* Raise a better user error when failing to evaluate a forward reference by @Viicos in [#10030](https://github.com/pydantic/pydantic/pull/10030)
* Fix evaluation of `__pydantic_extra__` annotation in specific circumstances by @Viicos in [#10070](https://github.com/pydantic/pydantic/pull/10070)
* Fix `frozen` enforcement for `dataclasses` by @sydney-runkle in [#10066](https://github.com/pydantic/pydantic/pull/10066)
* Remove logic to handle unused `__get_pydantic_core_schema__` signature by @Viicos in [#10075](https://github.com/pydantic/pydantic/pull/10075)
* Use `is_annotated` consistently by @Viicos in [#10095](https://github.com/pydantic/pydantic/pull/10095)
* Fix `PydanticDeprecatedSince26` typo by @kc0506 in [#10101](https://github.com/pydantic/pydantic/pull/10101)
* Improve `pyright` tests, refactor model decorators signatures by @Viicos in [#10092](https://github.com/pydantic/pydantic/pull/10092)
* Fix `ip` serialization logic by @sydney-runkle in [#10112](https://github.com/pydantic/pydantic/pull/10112)
* Warn when frozen defined twice for `dataclasses` by @mochi22 in [#10082](https://github.com/pydantic/pydantic/pull/10082)
* Do not compute JSON Schema default when plain serializers are used with `when_used` set to `'json-unless-none'` and the default value is `None` by @Viicos in [#10121](https://github.com/pydantic/pydantic/pull/10121)
* Fix `ImportString` special cases by @sydney-runkle in [#10137](https://github.com/pydantic/pydantic/pull/10137)
* Blacklist default globals to support exotic user code with `__` prefixed annotations by @sydney-runkle in [#10136](https://github.com/pydantic/pydantic/pull/10136)
* Handle `nullable` schemas with `serialization` schema available during JSON Schema generation by @Viicos in [#10132](https://github.com/pydantic/pydantic/pull/10132)
* Reorganize `BaseModel` annotations by @kc0506 in [#10110](https://github.com/pydantic/pydantic/pull/10110)
* Fix core schema simplification when serialization schemas are involved in specific scenarios by @Viicos in [#10155](https://github.com/pydantic/pydantic/pull/10155)
* Add support for stringified annotations when using `PrivateAttr` with `Annotated` by @Viicos in [#10157](https://github.com/pydantic/pydantic/pull/10157)
* Fix JSON Schema `number` type for literal and enum schemas by @Viicos in [#10172](https://github.com/pydantic/pydantic/pull/10172)
* Fix JSON Schema generation of fields with plain validators in serialization mode by @Viicos in [#10167](https://github.com/pydantic/pydantic/pull/10167)
* Fix invalid JSON Schemas being generated for functions in certain scenarios by @Viicos in [#10188](https://github.com/pydantic/pydantic/pull/10188)
* Make sure generated JSON Schemas are valid in tests by @Viicos in [#10182](https://github.com/pydantic/pydantic/pull/10182)
* Fix key error with custom serializer by @sydney-runkle in [#10200](https://github.com/pydantic/pydantic/pull/10200)
* Add 'wss' for allowed schemes in NatsDsn by @swelborn in [#10224](https://github.com/pydantic/pydantic/pull/10224)
* Fix `Mapping` and `MutableMapping` annotations to use mapping schema instead of dict schema by @sydney-runkle in [#10020](https://github.com/pydantic/pydantic/pull/10020)
* Fix JSON Schema generation for constrained dates by @Viicos in [#10185](https://github.com/pydantic/pydantic/pull/10185)
* Fix discriminated union bug regression when using enums by @kfreezen in [pydantic/pydantic-core#1286](https://github.com/pydantic/pydantic-core/pull/1286)
* Fix `field_serializer` with computed field when using `*` by @nix010 in [pydantic/pydantic-core#1349](https://github.com/pydantic/pydantic-core/pull/1349)
* Try each option in `Union` serializer before inference by @sydney-runkle in [pydantic/pydantic-core#1398](https://github.com/pydantic/pydantic-core/pull/1398)
* Fix `float` serialization behavior in `strict` mode by @sydney-runkle in [pydantic/pydantic-core#1400](https://github.com/pydantic/pydantic-core/pull/1400)
* Introduce `exactness` into Decimal validation logic to improve union validation behavior by @sydney-runkle in in [pydantic/pydantic-core#1405](https://github.com/pydantic/pydantic-core/pull/1405)
* Fix new warnings assertions to use `pytest.warns()` by @mgorny in [#10241](https://github.com/pydantic/pydantic/pull/10241)
* Fix a crash when cleaning the namespace in `ModelMetaclass` by @Viicos in [#10242](https://github.com/pydantic/pydantic/pull/10242)
* Fix parent namespace issue with model rebuilds by @sydney-runkle in [#10257](https://github.com/pydantic/pydantic/pull/10257)
* Remove defaults filter for namespace by @sydney-runkle in [#10261](https://github.com/pydantic/pydantic/pull/10261)
* Use identity instead of equality after validating model in `__init__` by @Viicos in [#10264](https://github.com/pydantic/pydantic/pull/10264)
* Support `BigInt` serialization for `int` subclasses by @kxx317 in [pydantic/pydantic-core#1417](https://github.com/pydantic/pydantic-core/pull/1417)
* Support signature for wrap validators without `info` by @sydney-runkle in [#10277](https://github.com/pydantic/pydantic/pull/10277)
* Ensure `__pydantic_complete__` is set when rebuilding `dataclasses` by @Viicos in [#10291](https://github.com/pydantic/pydantic/pull/10291)
* Respect `schema_generator` config value in `TypeAdapter` by @sydney-runkle in [#10300](https://github.com/pydantic/pydantic/pull/10300)

### New Contributors

#### `pydantic`

* @kwint made their first contribution in [#9787](https://github.com/pydantic/pydantic/pull/9787)
* @seekinginfiniteloop made their first contribution in [#9822](https://github.com/pydantic/pydantic/pull/9822)
* @a-alexander made their first contribution in [#9848](https://github.com/pydantic/pydantic/pull/9848)
* @maximilianfellhuber made their first contribution in [#9885](https://github.com/pydantic/pydantic/pull/9885)
* @karmaBonfire made their first contribution in [#9945](https://github.com/pydantic/pydantic/pull/9945)
* @s-rigaud made their first contribution in [#9958](https://github.com/pydantic/pydantic/pull/9958)
* @msabramo made their first contribution in [#9964](https://github.com/pydantic/pydantic/pull/9964)
* @DimaCybr made their first contribution in [#9972](https://github.com/pydantic/pydantic/pull/9972)
* @kc0506 made their first contribution in [#9971](https://github.com/pydantic/pydantic/pull/9971)
* @haoyun made their first contribution in [#9990](https://github.com/pydantic/pydantic/pull/9990)
* @radekwlsk made their first contribution in [#9938](https://github.com/pydantic/pydantic/pull/9938)
* @dpeachey made their first contribution in [#10029](https://github.com/pydantic/pydantic/pull/10029)
* @BoxyUwU made their first contribution in [#10085](https://github.com/pydantic/pydantic/pull/10085)
* @mochi22 made their first contribution in [#10082](https://github.com/pydantic/pydantic/pull/10082)
* @aditkumar72 made their first contribution in [#10128](https://github.com/pydantic/pydantic/pull/10128)
* @changhc made their first contribution in [#9654](https://github.com/pydantic/pydantic/pull/9654)
* @insumanth made their first contribution in [#10229](https://github.com/pydantic/pydantic/pull/10229)
* @AdolfoVillalobos made their first contribution in [#10240](https://github.com/pydantic/pydantic/pull/10240)
* @bllchmbrs made their first contribution in [#10270](https://github.com/pydantic/pydantic/pull/10270)

#### `pydantic-core`

* @kfreezen made their first contribution in [pydantic/pydantic-core#1286](https://github.com/pydantic/pydantic-core/pull/1286)
* @tinez made their first contribution in [pydantic/pydantic-core#1368](https://github.com/pydantic/pydantic-core/pull/1368)
* @fft001 made their first contribution in [pydantic/pydantic-core#1362](https://github.com/pydantic/pydantic-core/pull/1362)
* @nix010 made their first contribution in [pydantic/pydantic-core#1349](https://github.com/pydantic/pydantic-core/pull/1349)
* @BoxyUwU made their first contribution in [pydantic/pydantic-core#1379](https://github.com/pydantic/pydantic-core/pull/1379)
* @candleindark made their first contribution in [pydantic/pydantic-core#1404](https://github.com/pydantic/pydantic-core/pull/1404)
* @changhc made their first contribution in [pydantic/pydantic-core#1331](https://github.com/pydantic/pydantic-core/pull/1331)

## v2.9.0b2 (2024-08-30)

Pre-release, see [the GitHub release](https://github.com/pydantic/pydantic/releases/tag/v2.9.0b2) for details.

## v2.9.0b1 (2024-08-26)

Pre-release, see [the GitHub release](https://github.com/pydantic/pydantic/releases/tag/v2.9.0b1) for details.

## v2.8.2 (2024-07-03)

[GitHub release](https://github.com/pydantic/pydantic/releases/tag/v2.8.2)

### What's Changed

#### Fixes

* Fix issue with assertion caused by pluggable schema validator by @dmontagu in [#9838](https://github.com/pydantic/pydantic/pull/9838)

## v2.8.1 (2024-07-03)

[GitHub release](https://github.com/pydantic/pydantic/releases/tag/v2.8.1)

### What's Changed

#### Packaging

* Bump `ruff` to `v0.5.0` and `pyright` to `v1.1.369` by @sydney-runkle in [#9801](https://github.com/pydantic/pydantic/pull/9801)
* Bump `pydantic-core` to `v2.20.1`, `pydantic-extra-types` to `v2.9.0` by @sydney-runkle in [#9832](https://github.com/pydantic/pydantic/pull/9832)

#### Fixes

* Fix breaking change in `to_snake` from v2.7 -> v2.8 by @sydney-runkle in [#9812](https://github.com/pydantic/pydantic/pull/9812)
* Fix list constraint json schema application by @sydney-runkle in [#9818](https://github.com/pydantic/pydantic/pull/9818)
* Support time duration more than 23 by @nix010 in [pydantic/speedate#64](https://github.com/pydantic/speedate/pull/64)
* Fix millisecond fraction being handled with the wrong scale by @davidhewitt in [pydantic/speedate#65](https://github.com/pydantic/speedate/pull/65)
* Handle negative fractional durations correctly by @sydney-runkle in [pydantic/speedate#71](https://github.com/pydantic/speedate/pull/71)

## v2.8.0 (2024-07-01)

[GitHub release](https://github.com/pydantic/pydantic/releases/tag/v2.8.0)

The code released in v2.8.0 is functionally identical to that of v2.8.0b1.

### What's Changed

#### Packaging

* Update citation version automatically with new releases by @sydney-runkle in [#9673](https://github.com/pydantic/pydantic/pull/9673)
* Bump pyright to `v1.1.367` and add type checking tests for pipeline API by @adriangb in [#9674](https://github.com/pydantic/pydantic/pull/9674)
* Update `pydantic.v1` stub to `v1.10.17` by @sydney-runkle in [#9707](https://github.com/pydantic/pydantic/pull/9707)
* General package updates to prep for `v2.8.0b1` by @sydney-runkle in [#9741](https://github.com/pydantic/pydantic/pull/9741)
* Bump `pydantic-core` to `v2.20.0` by @sydney-runkle in [#9745](https://github.com/pydantic/pydantic/pull/9745)
* Add support for Python 3.13 by @sydney-runkle in [#9743](https://github.com/pydantic/pydantic/pull/9743)
* Update `pdm` version used for `pdm.lock` to v2.16.1 by @sydney-runkle in [#9761](https://github.com/pydantic/pydantic/pull/9761)
* Update to `ruff` `v0.4.8` by @Viicos in [#9585](https://github.com/pydantic/pydantic/pull/9585)

#### New Features

* Experimental: support `defer_build` for `TypeAdapter` by @MarkusSintonen in [#8939](https://github.com/pydantic/pydantic/pull/8939)
* Implement `deprecated` field in json schema by @NeevCohen in [#9298](https://github.com/pydantic/pydantic/pull/9298)
* Experimental: Add pipeline API by @adriangb in [#9459](https://github.com/pydantic/pydantic/pull/9459)
* Add support for programmatic title generation by @NeevCohen in [#9183](https://github.com/pydantic/pydantic/pull/9183)
* Implement `fail_fast` feature by @uriyyo in [#9708](https://github.com/pydantic/pydantic/pull/9708)
* Add `ser_json_inf_nan='strings'` mode to produce valid JSON by @josh-newman in [pydantic/pydantic-core#1307](https://github.com/pydantic/pydantic-core/pull/1307)

#### Changes

* Add warning when "alias" is set in ignored `Annotated` field by @nix010 in [#9170](https://github.com/pydantic/pydantic/pull/9170)
* Support serialization of some serializable defaults in JSON schema by @sydney-runkle in [#9624](https://github.com/pydantic/pydantic/pull/9624)
* Relax type specification for `__validators__` values in `create_model` by @sydney-runkle in [#9697](https://github.com/pydantic/pydantic/pull/9697)
* **Breaking Change:** Improve `smart` union matching logic by @sydney-runkle in [pydantic/pydantic-core#1322](https://github.com/pydantic/pydantic-core/pull/1322)
You can read more about our `smart` union matching logic [here](https://docs.pydantic.dev/dev/concepts/unions/#smart-mode). In some cases, if the old behavior
is desired, you can switch to `left-to-right` mode and change the order of your `Union` members.

#### Performance

##### Internal Improvements

* ⚡️ Speed up `_display_error_loc()` by 25% in `pydantic/v1/error_wrappers.py` by @misrasaurabh1 in [#9653](https://github.com/pydantic/pydantic/pull/9653)
* ⚡️ Speed up `_get_all_json_refs()` by 34% in `pydantic/json_schema.py` by @misrasaurabh1 in [#9650](https://github.com/pydantic/pydantic/pull/9650)
* ⚡️ Speed up `is_pydantic_dataclass()` by 41% in `pydantic/dataclasses.py` by @misrasaurabh1 in [#9652](https://github.com/pydantic/pydantic/pull/9652)
* ⚡️ Speed up `to_snake()` by 27% in `pydantic/alias_generators.py` by @misrasaurabh1 in [#9747](https://github.com/pydantic/pydantic/pull/9747)
* ⚡️ Speed up `unwrap_wrapped_function()` by 93% in `pydantic/_internal/_decorators.py` by @misrasaurabh1 in [#9727](https://github.com/pydantic/pydantic/pull/9727)

#### Fixes

* Replace `__spec__.parent` with `__package__` by @hramezani in [#9331](https://github.com/pydantic/pydantic/pull/9331)
* Fix Outputted Model JSON Schema for `Sequence` type by @anesmemisevic in [#9303](https://github.com/pydantic/pydantic/pull/9303)
* Fix typing of `_frame_depth` by @Viicos in [#9353](https://github.com/pydantic/pydantic/pull/9353)
* Make `ImportString` json schema compatible by @amitschang in [#9344](https://github.com/pydantic/pydantic/pull/9344)
* Hide private attributes (`PrivateAttr`) from `__init__` signature in type checkers by @idan22moral in [#9293](https://github.com/pydantic/pydantic/pull/9293)
* Make detection of `TypeVar` defaults robust to the CPython `PEP-696` implementation by @AlexWaygood in [#9426](https://github.com/pydantic/pydantic/pull/9426)
* Fix usage of `PlainSerializer` with builtin types by @Viicos in [#9450](https://github.com/pydantic/pydantic/pull/9450)
* Add more robust custom validation examples by @ChrisPappalardo in [#9468](https://github.com/pydantic/pydantic/pull/9468)
* Fix ignored `strict` specification for `StringConstraint(strict=False)` by @vbmendes in [#9476](https://github.com/pydantic/pydantic/pull/9476)
* **Breaking Change:** Use PEP 570 syntax by @Viicos in [#9479](https://github.com/pydantic/pydantic/pull/9479)
* Use `Self` where possible by @Viicos in [#9479](https://github.com/pydantic/pydantic/pull/9479)
* Do not alter `RootModel.model_construct` signature in the `mypy` plugin by @Viicos in [#9480](https://github.com/pydantic/pydantic/pull/9480)
* Fixed type hint of `validation_context` by @OhioDschungel6 in [#9508](https://github.com/pydantic/pydantic/pull/9508)
* Support context being passed to TypeAdapter's `dump_json`/`dump_python` by @alexcouper in [#9495](https://github.com/pydantic/pydantic/pull/9495)
* Updates type signature for `Field()` constructor by @bjmc in [#9484](https://github.com/pydantic/pydantic/pull/9484)
* Improve builtin alias generators by @sydney-runkle in [#9561](https://github.com/pydantic/pydantic/pull/9561)
* Fix typing of `TypeAdapter` by @Viicos in [#9570](https://github.com/pydantic/pydantic/pull/9570)
* Add fallback default value for private fields in `__setstate__` of BaseModel by @anhpham1509 in [#9584](https://github.com/pydantic/pydantic/pull/9584)
* Support `PEP 746` by @adriangb in [#9587](https://github.com/pydantic/pydantic/pull/9587)
* Allow validator and serializer functions to have default values by @Viicos in [#9478](https://github.com/pydantic/pydantic/pull/9478)
* Fix bug with mypy plugin's handling of covariant `TypeVar` fields by @dmontagu in [#9606](https://github.com/pydantic/pydantic/pull/9606)
* Fix multiple annotation / constraint application logic by @sydney-runkle in [#9623](https://github.com/pydantic/pydantic/pull/9623)
* Respect `regex` flags in validation and json schema by @sydney-runkle in [#9591](https://github.com/pydantic/pydantic/pull/9591)
* Fix type hint on `IpvAnyAddress` by @sydney-runkle in [#9640](https://github.com/pydantic/pydantic/pull/9640)
* Allow a field specifier on `__pydantic_extra__` by @dmontagu in [#9659](https://github.com/pydantic/pydantic/pull/9659)
* Use normalized case for file path comparison by @sydney-runkle in [#9737](https://github.com/pydantic/pydantic/pull/9737)
* Modify constraint application logic to allow field constraints on `Optional[Decimal]` by @lazyhope in [#9754](https://github.com/pydantic/pydantic/pull/9754)
* `validate_call` type params fix by @sydney-runkle in [#9760](https://github.com/pydantic/pydantic/pull/9760)
* Check all warnings returned by pytest.warns() by @s-t-e-v-e-n-k in [#9702](https://github.com/pydantic/pydantic/pull/9702)
* Reuse `re.Pattern` object in regex patterns to allow for regex flags by @sydney-runkle in [pydantic/pydantic-core#1318](https://github.com/pydantic/pydantic-core/pull/1318)

### New Contributors

* @idan22moral made their first contribution in [#9294](https://github.com/pydantic/pydantic/pull/9294)
* @anesmemisevic made their first contribution in [#9303](https://github.com/pydantic/pydantic/pull/9303)
* @max-muoto made their first contribution in [#9338](https://github.com/pydantic/pydantic/pull/9338)
* @amitschang made their first contribution in [#9344](https://github.com/pydantic/pydantic/pull/9344)
* @paulmartin91 made their first contribution in [#9410](https://github.com/pydantic/pydantic/pull/9410)
* @OhioDschungel6 made their first contribution in [#9405](https://github.com/pydantic/pydantic/pull/9405)
* @AlexWaygood made their first contribution in [#9426](https://github.com/pydantic/pydantic/pull/9426)
* @kinuax made their first contribution in [#9433](https://github.com/pydantic/pydantic/pull/9433)
* @antoni-jamiolkowski made their first contribution in [#9431](https://github.com/pydantic/pydantic/pull/9431)
* @candleindark made their first contribution in [#9448](https://github.com/pydantic/pydantic/pull/9448)
* @nix010 made their first contribution in [#9170](https://github.com/pydantic/pydantic/pull/9170)
* @tomy0000000 made their first contribution in [#9457](https://github.com/pydantic/pydantic/pull/9457)
* @vbmendes made their first contribution in [#9470](https://github.com/pydantic/pydantic/pull/9470)
* @micheleAlberto made their first contribution in [#9471](https://github.com/pydantic/pydantic/pull/9471)
* @ChrisPappalardo made their first contribution in [#9468](https://github.com/pydantic/pydantic/pull/9468)
* @blueTurtz made their first contribution in [#9475](https://github.com/pydantic/pydantic/pull/9475)
* @WinterBlue16 made their first contribution in [#9477](https://github.com/pydantic/pydantic/pull/9477)
* @bittner made their first contribution in [#9500](https://github.com/pydantic/pydantic/pull/9500)
* @alexcouper made their first contribution in [#9495](https://github.com/pydantic/pydantic/pull/9495)
* @bjmc made their first contribution in [#9484](https://github.com/pydantic/pydantic/pull/9484)
* @pjvv made their first contribution in [#9529](https://github.com/pydantic/pydantic/pull/9529)
* @nedbat made their first contribution in [#9530](https://github.com/pydantic/pydantic/pull/9530)
* @gunnellEvan made their first contribution in [#9469](https://github.com/pydantic/pydantic/pull/9469)
* @jaymbans made their first contribution in [#9531](https://github.com/pydantic/pydantic/pull/9531)
* @MarcBresson made their first contribution in [#9534](https://github.com/pydantic/pydantic/pull/9534)
* @anhpham1509 made their first contribution in [#9584](https://github.com/pydantic/pydantic/pull/9584)
* @K-dash made their first contribution in [#9595](https://github.com/pydantic/pydantic/pull/9595)
* @s-t-e-v-e-n-k made their first contribution in [#9527](https://github.com/pydantic/pydantic/pull/9527)
* @airwoodix made their first contribution in [#9506](https://github.com/pydantic/pydantic/pull/9506)
* @misrasaurabh1 made their first contribution in [#9653](https://github.com/pydantic/pydantic/pull/9653)
* @AlessandroMiola made their first contribution in [#9740](https://github.com/pydantic/pydantic/pull/9740)
* @mylapallilavanyaa made their first contribution in [#9746](https://github.com/pydantic/pydantic/pull/9746)
* @lazyhope made their first contribution in [#9754](https://github.com/pydantic/pydantic/pull/9754)
* @YassinNouh21 made their first contribution in [#9759](https://github.com/pydantic/pydantic/pull/9759)

## v2.8.0b1 (2024-06-27)

Pre-release, see [the GitHub release](https://github.com/pydantic/pydantic/releases/tag/v2.8.0b1) for details.

## v2.7.4 (2024-06-12)

[Github release](https://github.com/pydantic/pydantic/releases/tag/v2.7.4)

### What's Changed

#### Packaging

* Bump `pydantic.v1` to `v1.10.16` reference by @sydney-runkle in [#9639](https://github.com/pydantic/pydantic/pull/9639)

#### Fixes

* Specify `recursive_guard` as kwarg in `FutureRef._evaluate` by @vfazio in [#9612](https://github.com/pydantic/pydantic/pull/9612)

## v2.7.3 (2024-06-03)

[GitHub release](https://github.com/pydantic/pydantic/releases/tag/v2.7.3)

### What's Changed

#### Packaging

* Bump `pydantic-core` to `v2.18.4` by @sydney-runkle in [#9550](https://github.com/pydantic/pydantic/pull/9550)

#### Fixes

* Fix u style unicode strings in python @samuelcolvin in [pydantic/jiter#110](https://github.com/pydantic/jiter/pull/110)

## v2.7.2 (2024-05-28)

[GitHub release](https://github.com/pydantic/pydantic/releases/tag/v2.7.2)

### What's Changed

#### Packaging

* Bump `pydantic-core` to `v2.18.3` by @sydney-runkle in [#9515](https://github.com/pydantic/pydantic/pull/9515)

#### Fixes

* Replace `__spec__.parent` with `__package__` by @hramezani in [#9331](https://github.com/pydantic/pydantic/pull/9331)
* Fix validation of `int`s with leading unary minus by @RajatRajdeep in [pydantic/pydantic-core#1291](https://github.com/pydantic/pydantic-core/pull/1291)
* Fix `str` subclass validation for enums by @sydney-runkle in [pydantic/pydantic-core#1273](https://github.com/pydantic/pydantic-core/pull/1273)
* Support `BigInt`s in `Literal`s and `Enum`s by @samuelcolvin in [pydantic/pydantic-core#1297](https://github.com/pydantic/pydantic-core/pull/1297)
* Fix: uuid - allow `str` subclass as input by @davidhewitt in [pydantic/pydantic-core#1296](https://github.com/pydantic/pydantic-core/pull/1296)

## v2.7.1 (2024-04-23)

[GitHub release](https://github.com/pydantic/pydantic/releases/tag/v2.7.1)

### What's Changed

#### Packaging

* Bump `pydantic-core` to `v2.18.2` by @sydney-runkle in [#9307](https://github.com/pydantic/pydantic/pull/9307)

#### New Features

* Ftp and Websocket connection strings support by @CherrySuryp in [#9205](https://github.com/pydantic/pydantic/pull/9205)

#### Changes

* Use field description for RootModel schema description when there is `…` by @LouisGobert in [#9214](https://github.com/pydantic/pydantic/pull/9214)

#### Fixes

* Fix `validation_alias` behavior with `model_construct` for `AliasChoices` and `AliasPath` by @sydney-runkle in [#9223](https://github.com/pydantic/pydantic/pull/9223)
* Revert `typing.Literal` and import it outside the TYPE_CHECKING block by @frost-nzcr4 in [#9232](https://github.com/pydantic/pydantic/pull/9232)
* Fix `Secret` serialization schema, applicable for unions by @sydney-runkle in [#9240](https://github.com/pydantic/pydantic/pull/9240)
* Fix `strict` application to `function-after` with `use_enum_values` by @sydney-runkle in [#9279](https://github.com/pydantic/pydantic/pull/9279)
* Address case where `model_construct` on a class which defines `model_post_init` fails with `AttributeError` by @babygrimes in [#9168](https://github.com/pydantic/pydantic/pull/9168)
* Fix `model_json_schema` with config types by @NeevCohen in [#9287](https://github.com/pydantic/pydantic/pull/9287)
* Support multiple zeros as an `int` by @samuelcolvin in [pydantic/pydantic-core#1269](https://github.com/pydantic/pydantic-core/pull/1269)
* Fix validation of `int`s with leading unary plus by @cknv in [pydantic/pydantic-core#1272](https://github.com/pydantic/pydantic-core/pull/1272)
* Fix interaction between `extra != 'ignore'` and `from_attributes=True` by @davidhewitt in [pydantic/pydantic-core#1276](https://github.com/pydantic/pydantic-core/pull/1276)
* Handle error from `Enum`'s `missing` function as `ValidationError` by @sydney-runkle in [pydantic/pydantic-core#1274](https://github.com/pydantic/pydantic-core/pull/1754)
* Fix memory leak with `Iterable` validation by @davidhewitt in [pydantic/pydantic-core#1271](https://github.com/pydantic/pydantic-core/pull/1751)

### New Contributors

* @zzstoatzz made their first contribution in [#9219](https://github.com/pydantic/pydantic/pull/9219)
* @frost-nzcr4 made their first contribution in [#9232](https://github.com/pydantic/pydantic/pull/9232)
* @CherrySuryp made their first contribution in [#9205](https://github.com/pydantic/pydantic/pull/9205)
* @vagenas made their first contribution in [#9268](https://github.com/pydantic/pydantic/pull/9268)
* @ollz272 made their first contribution in [#9262](https://github.com/pydantic/pydantic/pull/9262)
* @babygrimes made their first contribution in [#9168](https://github.com/pydantic/pydantic/pull/9168)
* @swelborn made their first contribution in [#9296](https://github.com/pydantic/pydantic/pull/9296)
* @kf-novi made their first contribution in [#9236](https://github.com/pydantic/pydantic/pull/9236)
* @lgeiger made their first contribution in [#9288](https://github.com/pydantic/pydantic/pull/9288)

## v2.7.0 (2024-04-11)

[GitHub release](https://github.com/pydantic/pydantic/releases/tag/v2.7.0)

The code released in v2.7.0 is practically identical to that of v2.7.0b1.

### What's Changed

#### Packaging

* Reorganize `pyproject.toml` sections by @Viicos in [#8899](https://github.com/pydantic/pydantic/pull/8899)
* Bump `pydantic-core` to `v2.18.1` by @sydney-runkle in [#9211](https://github.com/pydantic/pydantic/pull/9211)
* Adopt `jiter` `v0.2.0` by @samuelcolvin in [pydantic/pydantic-core#1250](https://github.com/pydantic/pydantic-core/pull/1250)

#### New Features

* Extract attribute docstrings from `FieldInfo.description` by @Viicos in [#6563](https://github.com/pydantic/pydantic/pull/6563)
* Add a `with_config` decorator to comply with typing spec by @Viicos in [#8611](https://github.com/pydantic/pydantic/pull/8611)
* Allow an optional separator splitting the value and unit of the result of `ByteSize.human_readable` by @jks15satoshi in [#8706](https://github.com/pydantic/pydantic/pull/8706)
* Add generic `Secret` base type by @conradogarciaberrotaran in [#8519](https://github.com/pydantic/pydantic/pull/8519)
* Make use of `Sphinx` inventories for cross references in docs by @Viicos in [#8682](https://github.com/pydantic/pydantic/pull/8682)
* Add environment variable to disable plugins by @geospackle in [#8767](https://github.com/pydantic/pydantic/pull/8767)
* Add support for `deprecated` fields by @Viicos in [#8237](https://github.com/pydantic/pydantic/pull/8237)
* Allow `field_serializer('*')` by @ornariece in [#9001](https://github.com/pydantic/pydantic/pull/9001)
* Handle a case when `model_config` is defined as a model property by @alexeyt101 in [#9004](https://github.com/pydantic/pydantic/pull/9004)
* Update `create_model()` to support `typing.Annotated` as input by @wannieman98 in [#8947](https://github.com/pydantic/pydantic/pull/8947)
* Add `ClickhouseDsn` support by @solidguy7 in [#9062](https://github.com/pydantic/pydantic/pull/9062)
* Add support for `re.Pattern[str]` to `pattern` field by @jag-k in [#9053](https://github.com/pydantic/pydantic/pull/9053)
* Support for `serialize_as_any` runtime setting by @sydney-runkle in [#8830](https://github.com/pydantic/pydantic/pull/8830)
* Add support for `typing.Self` by @Youssefares in [#9023](https://github.com/pydantic/pydantic/pull/9023)
* Ability to pass `context` to serialization by @ornariece in [#8965](https://github.com/pydantic/pydantic/pull/8965)
* Add feedback widget to docs with flarelytics integration by @sydney-runkle in [#9129](https://github.com/pydantic/pydantic/pull/9129)
* Support for parsing partial JSON strings in Python by @samuelcolvin in [pydantic/jiter#66](https://github.com/pydantic/jiter/pull/66)

**Finalized in v2.7.0, rather than v2.7.0b1:**

* Add support for field level number to str coercion option by @NeevCohen in [#9137](https://github.com/pydantic/pydantic/pull/9137)
* Update `warnings` parameter for serialization utilities to allow raising a warning by @Lance-Drane in [#9166](https://github.com/pydantic/pydantic/pull/9166)

#### Changes

* Correct docs, logic for `model_construct` behavior with `extra` by @sydney-runkle in [#8807](https://github.com/pydantic/pydantic/pull/8807)
* Improve error message for improper `RootModel` subclasses by @sydney-runkle in [#8857](https://github.com/pydantic/pydantic/pull/8857)
* **Breaking Change:** Use `PEP570` syntax by @Viicos in [#8940](https://github.com/pydantic/pydantic/pull/8940)
* Add `enum` and `type` to the JSON schema for single item literals by @dmontagu in [#8944](https://github.com/pydantic/pydantic/pull/8944)
* Deprecate `update_json_schema` internal function by @sydney-runkle in [#9125](https://github.com/pydantic/pydantic/pull/9125)
* Serialize duration to hour minute second, instead of just seconds by @kakilangit in [pydantic/speedate#50](https://github.com/pydantic/speedate/pull/50)
* Trimming str before parsing to int and float by @hungtsetse in [pydantic/pydantic-core#1203](https://github.com/pydantic/pydantic-core/pull/1203)

#### Performance

* `enum` validator improvements by @samuelcolvin in [#9045](https://github.com/pydantic/pydantic/pull/9045)
* Move `enum` validation and serialization to Rust by @samuelcolvin in [#9064](https://github.com/pydantic/pydantic/pull/9064)
* Improve schema generation for nested dataclasses by @sydney-runkle in [#9114](https://github.com/pydantic/pydantic/pull/9114)
* Fast path for ASCII python string creation in JSON by @samuelcolvin in in [pydantic/jiter#72](https://github.com/pydantic/jiter/pull/72)
* SIMD integer and string JSON parsing on `aarch64`(**Note:** SIMD on x86 will be implemented in a future release) by @samuelcolvin in in [pydantic/jiter#65](https://github.com/pydantic/jiter/pull/65)
* Support JSON `Cow<str>` from `jiter` by @davidhewitt in [pydantic/pydantic-core#1231](https://github.com/pydantic/pydantic-core/pull/1231)
* MAJOR performance improvement: update to PyO3 0.21 final by @davidhewitt in [pydantic/pydantic-core#1248](https://github.com/pydantic/pydantic-core/pull/1248)
* cache Python strings by @samuelcolvin in [pydantic/pydantic-core#1240](https://github.com/pydantic/pydantic-core/pull/1240)

#### Fixes

* Fix strict parsing for some `Sequence`s by @sydney-runkle in [#8614](https://github.com/pydantic/pydantic/pull/8614)
* Add a check on the existence of `__qualname__` by @anci3ntr0ck in [#8642](https://github.com/pydantic/pydantic/pull/8642)
* Handle `__pydantic_extra__` annotation being a string or inherited by @alexmojaki in [#8659](https://github.com/pydantic/pydantic/pull/8659)
* Fix json validation for `NameEmail` by @Holi0317 in [#8650](https://github.com/pydantic/pydantic/pull/8650)
* Fix type-safety of attribute access in `BaseModel` by @bluenote10 in [#8651](https://github.com/pydantic/pydantic/pull/8651)
* Fix bug with `mypy` plugin and `no_strict_optional = True` by @dmontagu in [#8666](https://github.com/pydantic/pydantic/pull/8666)
* Fix `ByteSize` error `type` change by @sydney-runkle in [#8681](https://github.com/pydantic/pydantic/pull/8681)
* Fix inheriting annotations in dataclasses by @sydney-runkle in [#8679](https://github.com/pydantic/pydantic/pull/8679)
* Fix regression in core schema generation for indirect definition references by @dmontagu in [#8702](https://github.com/pydantic/pydantic/pull/8702)
* Fix unsupported types bug with plain validator by @sydney-runkle in [#8710](https://github.com/pydantic/pydantic/pull/8710)
* Reverting problematic fix from 2.6 release, fixing schema building bug by @sydney-runkle in [#8718](https://github.com/pydantic/pydantic/pull/8718)
* fixes `__pydantic_config__` ignored for TypeDict by @13sin in [#8734](https://github.com/pydantic/pydantic/pull/8734)
* Fix test failures with `pytest v8.0.0` due to `pytest.warns()` starting to work inside `pytest.raises()` by @mgorny in [#8678](https://github.com/pydantic/pydantic/pull/8678)
* Use `is_valid_field` from 1.x for `mypy` plugin by @DanielNoord in [#8738](https://github.com/pydantic/pydantic/pull/8738)
* Better-support `mypy` strict equality flag by @dmontagu in [#8799](https://github.com/pydantic/pydantic/pull/8799)
* model_json_schema export with Annotated types misses 'required' parameters by @LouisGobert in [#8793](https://github.com/pydantic/pydantic/pull/8793)
* Fix default inclusion in `FieldInfo.__repr_args__` by @sydney-runkle in [#8801](https://github.com/pydantic/pydantic/pull/8801)
* Fix resolution of forward refs in dataclass base classes that are not present in the subclass module namespace by @matsjoyce-refeyn in [#8751](https://github.com/pydantic/pydantic/pull/8751)
* Fix `BaseModel` type annotations to be resolvable by `typing.get_type_hints` by @devmonkey22 in [#7680](https://github.com/pydantic/pydantic/pull/7680)
* Fix: allow empty string aliases with `AliasGenerator` by @sydney-runkle in [#8810](https://github.com/pydantic/pydantic/pull/8810)
* Fix test along with `date` -> `datetime` timezone assumption fix by @sydney-runkle in [#8823](https://github.com/pydantic/pydantic/pull/8823)
* Fix deprecation warning with usage of `ast.Str` by @Viicos in [#8837](https://github.com/pydantic/pydantic/pull/8837)
* Add missing `deprecated` decorators by @Viicos in [#8877](https://github.com/pydantic/pydantic/pull/8877)
* Fix serialization of `NameEmail` if name includes an email address by @NeevCohen in [#8860](https://github.com/pydantic/pydantic/pull/8860)
* Add information about class in error message of schema generation by @Czaki in [#8917](https://github.com/pydantic/pydantic/pull/8917)
* Make `TypeAdapter`'s typing compatible with special forms by @adriangb in [#8923](https://github.com/pydantic/pydantic/pull/8923)
* Fix issue with config behavior being baked into the ref schema for `enum`s by @dmontagu in [#8920](https://github.com/pydantic/pydantic/pull/8920)
* More helpful error re wrong `model_json_schema` usage by @sydney-runkle in [#8928](https://github.com/pydantic/pydantic/pull/8928)
* Fix nested discriminated union schema gen, pt 2 by @sydney-runkle in [#8932](https://github.com/pydantic/pydantic/pull/8932)
* Fix schema build for nested dataclasses / TypedDicts with discriminators by @sydney-runkle in [#8950](https://github.com/pydantic/pydantic/pull/8950)
* Remove unnecessary logic for definitions schema gen with discriminated unions by @sydney-runkle in [#8951](https://github.com/pydantic/pydantic/pull/8951)
* Fix handling of optionals in `mypy` plugin by @dmontagu in [#9008](https://github.com/pydantic/pydantic/pull/9008)
* Fix `PlainSerializer` usage with std type constructor by @sydney-runkle in [#9031](https://github.com/pydantic/pydantic/pull/9031)
* Remove unnecessary warning for config in plugin by @dmontagu in [#9039](https://github.com/pydantic/pydantic/pull/9039)
* Fix default value serializing by @NeevCohen in [#9066](https://github.com/pydantic/pydantic/pull/9066)
* Fix extra fields check in `Model.__getattr__()` by @NeevCohen in [#9082](https://github.com/pydantic/pydantic/pull/9082)
* Fix `ClassVar` forward ref inherited from parent class by @alexmojaki in [#9097](https://github.com/pydantic/pydantic/pull/9097)
* fix sequence like validator with strict `True` by @andresliszt in [#8977](https://github.com/pydantic/pydantic/pull/8977)
* Improve warning message when a field name shadows a field in a parent model by @chan-vince in [#9105](https://github.com/pydantic/pydantic/pull/9105)
* Do not warn about shadowed fields if they are not redefined in a child class by @chan-vince in [#9111](https://github.com/pydantic/pydantic/pull/9111)
* Fix discriminated union bug with unsubstituted type var by @sydney-runkle in [#9124](https://github.com/pydantic/pydantic/pull/9124)
* Support serialization of `deque` when passed to `Sequence[blah blah blah]` by @sydney-runkle in [#9128](https://github.com/pydantic/pydantic/pull/9128)
* Init private attributes from super-types in `model_post_init` by @Viicos in [#9134](https://github.com/pydantic/pydantic/pull/9134)
* fix `model_construct` with `validation_alias` by @ornariece in [#9144](https://github.com/pydantic/pydantic/pull/9144)
* Ensure json-schema generator handles `Literal` `null` types by @bruno-f-cruz in [#9135](https://github.com/pydantic/pydantic/pull/9135)
* **Fixed in v2.7.0**: Fix allow extra generic by @dmontagu in [#9193](https://github.com/pydantic/pydantic/pull/9193)

### New Contributors

* @hungtsetse made their first contribution in [#8546](https://github.com/pydantic/pydantic/pull/8546)
* @StrawHatDrag0n made their first contribution in [#8583](https://github.com/pydantic/pydantic/pull/8583)
* @anci3ntr0ck made their first contribution in [#8642](https://github.com/pydantic/pydantic/pull/8642)
* @Holi0317 made their first contribution in [#8650](https://github.com/pydantic/pydantic/pull/8650)
* @bluenote10 made their first contribution in [#8651](https://github.com/pydantic/pydantic/pull/8651)
* @ADSteele916 made their first contribution in [#8703](https://github.com/pydantic/pydantic/pull/8703)
* @musicinmybrain made their first contribution in [#8731](https://github.com/pydantic/pydantic/pull/8731)
* @jks15satoshi made their first contribution in [#8706](https://github.com/pydantic/pydantic/pull/8706)
* @13sin made their first contribution in [#8734](https://github.com/pydantic/pydantic/pull/8734)
* @DanielNoord made their first contribution in [#8738](https://github.com/pydantic/pydantic/pull/8738)
* @conradogarciaberrotaran made their first contribution in [#8519](https://github.com/pydantic/pydantic/pull/8519)
* @chris-griffin made their first contribution in [#8775](https://github.com/pydantic/pydantic/pull/8775)
* @LouisGobert made their first contribution in [#8793](https://github.com/pydantic/pydantic/pull/8793)
* @matsjoyce-refeyn made their first contribution in [#8751](https://github.com/pydantic/pydantic/pull/8751)
* @devmonkey22 made their first contribution in [#7680](https://github.com/pydantic/pydantic/pull/7680)
* @adamency made their first contribution in [#8847](https://github.com/pydantic/pydantic/pull/8847)
* @MamfTheKramf made their first contribution in [#8851](https://github.com/pydantic/pydantic/pull/8851)
* @ornariece made their first contribution in [#9001](https://github.com/pydantic/pydantic/pull/9001)
* @alexeyt101 made their first contribution in [#9004](https://github.com/pydantic/pydantic/pull/9004)
* @wannieman98 made their first contribution in [#8947](https://github.com/pydantic/pydantic/pull/8947)
* @solidguy7 made their first contribution in [#9062](https://github.com/pydantic/pydantic/pull/9062)
* @kloczek made their first contribution in [#9047](https://github.com/pydantic/pydantic/pull/9047)
* @jag-k made their first contribution in [#9053](https://github.com/pydantic/pydantic/pull/9053)
* @priya-gitTest made their first contribution in [#9088](https://github.com/pydantic/pydantic/pull/9088)
* @Youssefares made their first contribution in [#9023](https://github.com/pydantic/pydantic/pull/9023)
* @chan-vince made their first contribution in [#9105](https://github.com/pydantic/pydantic/pull/9105)
* @bruno-f-cruz made their first contribution in [#9135](https://github.com/pydantic/pydantic/pull/9135)
* @Lance-Drane made their first contribution in [#9166](https://github.com/pydantic/pydantic/pull/9166)

## v2.7.0b1 (2024-04-03)

Pre-release, see [the GitHub release](https://github.com/pydantic/pydantic/releases/tag/v2.7.0b1) for details.

## v2.6.4 (2024-03-12)

[GitHub release](https://github.com/pydantic/pydantic/releases/tag/v2.6.4)

### What's Changed

#### Fixes

* Fix usage of `AliasGenerator` with `computed_field` decorator by @sydney-runkle in [#8806](https://github.com/pydantic/pydantic/pull/8806)
* Fix nested discriminated union schema gen, pt 2 by @sydney-runkle in [#8932](https://github.com/pydantic/pydantic/pull/8932)
* Fix bug with no_strict_optional=True caused by API deferral by @dmontagu in [#8826](https://github.com/pydantic/pydantic/pull/8826)

## v2.6.3 (2024-02-27)

[GitHub release](https://github.com/pydantic/pydantic/releases/tag/v2.6.3)

### What's Changed

#### Packaging

* Update `pydantic-settings` version in the docs by @hramezani in [#8906](https://github.com/pydantic/pydantic/pull/8906)

#### Fixes

* Fix discriminated union schema gen bug by @sydney-runkle in [#8904](https://github.com/pydantic/pydantic/pull/8904)

## v2.6.2 (2024-02-23)

[GitHub release](https://github.com/pydantic/pydantic/releases/tag/v2.6.2)

### What's Changed

#### Packaging

* Upgrade to `pydantic-core` 2.16.3 by @sydney-runkle in [#8879](https://github.com/pydantic/pydantic/pull/8879)

#### Fixes

* 'YYYY-MM-DD' date string coerced to datetime shouldn't infer timezone by @sydney-runkle in [pydantic/pydantic-core#1193](https://github.com/pydantic/pydantic-core/pull/1193)

## v2.6.1 (2024-02-05)

[GitHub release](https://github.com/pydantic/pydantic/releases/tag/v2.6.1)

### What's Changed

#### Packaging

* Upgrade to `pydantic-core` 2.16.2 by @sydney-runkle in [#8717](https://github.com/pydantic/pydantic/pull/8717)

#### Fixes

* Fix bug with `mypy` plugin and `no_strict_optional = True` by @dmontagu in [#8666](https://github.com/pydantic/pydantic/pull/8666)
* Fix `ByteSize` error `type` change by @sydney-runkle in [#8681](https://github.com/pydantic/pydantic/pull/8681)
* Fix inheriting `Field` annotations in dataclasses by @sydney-runkle in [#8679](https://github.com/pydantic/pydantic/pull/8679)
* Fix regression in core schema generation for indirect definition references by @dmontagu in [#8702](https://github.com/pydantic/pydantic/pull/8702)
* Fix unsupported types bug with `PlainValidator` by @sydney-runkle in [#8710](https://github.com/pydantic/pydantic/pull/8710)
* Reverting problematic fix from 2.6 release, fixing schema building bug by @sydney-runkle in [#8718](https://github.com/pydantic/pydantic/pull/8718)
* Fix warning for tuple of wrong size in `Union` by @davidhewitt in [pydantic/pydantic-core#1174](https://github.com/pydantic/pydantic-core/pull/1174)
* Fix `computed_field` JSON serializer `exclude_none` behavior by @sydney-runkle in [pydantic/pydantic-core#1187](https://github.com/pydantic/pydantic-core/pull/1187)

## v2.6.0 (2024-01-23)

[GitHub release](https://github.com/pydantic/pydantic/releases/tag/v2.6.0)

The code released in v2.6.0 is practically identical to that of v2.6.0b1.

### What's Changed

#### Packaging

* Check for `email-validator` version >= 2.0 by @commonism in [#6033](https://github.com/pydantic/pydantic/pull/6033)
* Upgrade `ruff`` target version to Python 3.8 by @Elkiwa in [#8341](https://github.com/pydantic/pydantic/pull/8341)
* Update to `pydantic-extra-types==2.4.1` by @yezz123 in [#8478](https://github.com/pydantic/pydantic/pull/8478)
* Update to `pyright==1.1.345` by @Viicos in [#8453](https://github.com/pydantic/pydantic/pull/8453)
* Update pydantic-core from 2.14.6 to 2.16.1, significant changes from these updates are described below, full changelog [here](https://github.com/pydantic/pydantic-core/compare/v2.14.6...v2.16.1)

#### New Features

* Add `NatsDsn` by @ekeew in [#6874](https://github.com/pydantic/pydantic/pull/6874)
* Add `ConfigDict.ser_json_inf_nan` by @davidhewitt in [#8159](https://github.com/pydantic/pydantic/pull/8159)
* Add `types.OnErrorOmit` by @adriangb in [#8222](https://github.com/pydantic/pydantic/pull/8222)
* Support `AliasGenerator` usage by @sydney-runkle in [#8282](https://github.com/pydantic/pydantic/pull/8282)
* Add Pydantic People Page to docs by @sydney-runkle in [#8345](https://github.com/pydantic/pydantic/pull/8345)
* Support `yyyy-MM-DD` datetime parsing by @sydney-runkle in [#8404](https://github.com/pydantic/pydantic/pull/8404)
* Added bits conversions to the `ByteSize` class #8415 by @luca-matei in [#8507](https://github.com/pydantic/pydantic/pull/8507)
* Enable json schema creation with type `ByteSize` by @geospackle in [#8537](https://github.com/pydantic/pydantic/pull/8537)
* Add `eval_type_backport` to handle union operator and builtin generic subscripting in older Pythons by @alexmojaki in [#8209](https://github.com/pydantic/pydantic/pull/8209)
* Add support for `dataclass` fields `init` by @dmontagu in [#8552](https://github.com/pydantic/pydantic/pull/8552)
* Implement pickling for `ValidationError` by @davidhewitt in [pydantic/pydantic-core#1119](https://github.com/pydantic/pydantic-core/pull/1119)
* Add unified tuple validator that can handle "variadic" tuples via PEP-646 by @dmontagu in [pydantic/pydantic-core#865](https://github.com/pydantic/pydantic-core/pull/865)

#### Changes

* Drop Python3.7 support by @hramezani in [#7188](https://github.com/pydantic/pydantic/pull/7188)
* Drop Python 3.7, and PyPy 3.7 and 3.8 by @davidhewitt in [pydantic/pydantic-core#1129](https://github.com/pydantic/pydantic-core/pull/1129)
* Use positional-only `self` in `BaseModel` constructor, so no field name can ever conflict with it by @ariebovenberg in [#8072](https://github.com/pydantic/pydantic/pull/8072)
* Make `@validate_call` return a function instead of a custom descriptor - fixes binding issue with inheritance and adds `self/cls` argument to validation errors by @alexmojaki in [#8268](https://github.com/pydantic/pydantic/pull/8268)
* Exclude `BaseModel` docstring from JSON schema description by @sydney-runkle in [#8352](https://github.com/pydantic/pydantic/pull/8352)
* Introducing `classproperty` decorator for `model_computed_fields` by @Jocelyn-Gas in [#8437](https://github.com/pydantic/pydantic/pull/8437)
* Explicitly raise an error if field names clashes with types by @Viicos in [#8243](https://github.com/pydantic/pydantic/pull/8243)
* Use stricter serializer for unions of simple types by @alexdrydew [pydantic/pydantic-core#1132](https://github.com/pydantic/pydantic-core/pull/1132)

#### Performance

* Add Codspeed profiling Actions workflow  by @lambertsbennett in [#8054](https://github.com/pydantic/pydantic/pull/8054)
* Improve `int` extraction by @samuelcolvin in [pydantic/pydantic-core#1155](https://github.com/pydantic/pydantic-core/pull/1155)
* Improve performance of recursion guard by @samuelcolvin in [pydantic/pydantic-core#1156](https://github.com/pydantic/pydantic-core/pull/1156)
* `dataclass` serialization speedups by @samuelcolvin in [pydantic/pydantic-core#1162](https://github.com/pydantic/pydantic-core/pull/1162)
* Avoid `HashMap` creation when looking up small JSON objects in `LazyIndexMaps` by @samuelcolvin in [pydantic/jiter#55](https://github.com/pydantic/jiter/pull/55)
* use hashbrown to speedup python string caching by @davidhewitt in [pydantic/jiter#51](https://github.com/pydantic/jiter/pull/51)
* Replace `Peak` with more efficient `Peek` by @davidhewitt in [pydantic/jiter#48](https://github.com/pydantic/jiter/pull/48)

#### Fixes

* Move `getattr` warning in deprecated `BaseConfig` by @tlambert03 in [#7183](https://github.com/pydantic/pydantic/pull/7183)
* Only hash `model_fields`, not whole `__dict__` by @alexmojaki in [#7786](https://github.com/pydantic/pydantic/pull/7786)
* Fix mishandling of unions while freezing types in the `mypy` plugin by @dmontagu in [#7411](https://github.com/pydantic/pydantic/pull/7411)
* Fix `mypy` error on untyped `ClassVar` by @vincent-hachin-wmx in [#8138](https://github.com/pydantic/pydantic/pull/8138)
* Only compare pydantic fields in `BaseModel.__eq__` instead of whole `__dict__` by @QuentinSoubeyranAqemia in [#7825](https://github.com/pydantic/pydantic/pull/7825)
* Update `strict` docstring in `model_validate` method. by @LukeTonin in [#8223](https://github.com/pydantic/pydantic/pull/8223)
* Fix overload position of `computed_field` by @Viicos in [#8227](https://github.com/pydantic/pydantic/pull/8227)
* Fix custom type type casting used in multiple attributes by @ianhfc in [#8066](https://github.com/pydantic/pydantic/pull/8066)
* Fix issue not allowing `validate_call` decorator to be dynamically assigned to a class method by @jusexton in [#8249](https://github.com/pydantic/pydantic/pull/8249)
* Fix issue `unittest.mock` deprecation warnings  by @ibleedicare in [#8262](https://github.com/pydantic/pydantic/pull/8262)
* Added tests for the case `JsonValue` contains subclassed primitive values by @jusexton in [#8286](https://github.com/pydantic/pydantic/pull/8286)
* Fix `mypy` error on free before validator (classmethod) by @sydney-runkle in [#8285](https://github.com/pydantic/pydantic/pull/8285)
* Fix `to_snake` conversion by @jevins09 in [#8316](https://github.com/pydantic/pydantic/pull/8316)
* Fix type annotation of `ModelMetaclass.__prepare__` by @slanzmich in [#8305](https://github.com/pydantic/pydantic/pull/8305)
* Disallow `config` specification when initializing a `TypeAdapter` when the annotated type has config already by @sydney-runkle in [#8365](https://github.com/pydantic/pydantic/pull/8365)
* Fix a naming issue with JSON schema for generics parametrized by recursive type aliases by @dmontagu in [#8389](https://github.com/pydantic/pydantic/pull/8389)
* Fix type annotation in pydantic people script by @shenxiangzhuang in [#8402](https://github.com/pydantic/pydantic/pull/8402)
* Add support for field `alias` in `dataclass` signature by @NeevCohen in [#8387](https://github.com/pydantic/pydantic/pull/8387)
* Fix bug with schema generation with `Field(...)` in a forward ref by @dmontagu in [#8494](https://github.com/pydantic/pydantic/pull/8494)
* Fix ordering of keys in `__dict__` with `model_construct` call by @sydney-runkle in [#8500](https://github.com/pydantic/pydantic/pull/8500)
* Fix module `path_type` creation when globals does not contain `__name__` by @hramezani in [#8470](https://github.com/pydantic/pydantic/pull/8470)
* Fix for namespace issue with dataclasses with `from __future__ import annotations` by @sydney-runkle in [#8513](https://github.com/pydantic/pydantic/pull/8513)
* Fix: make function validator types positional-only by @pmmmwh in [#8479](https://github.com/pydantic/pydantic/pull/8479)
* Fix usage of `@deprecated` by @Viicos in [#8294](https://github.com/pydantic/pydantic/pull/8294)
* Add more support for private attributes in `model_construct` call by @sydney-runkle in [#8525](https://github.com/pydantic/pydantic/pull/8525)
* Use a stack for the types namespace by @dmontagu in [#8378](https://github.com/pydantic/pydantic/pull/8378)
* Fix schema-building bug with `TypeAliasType` for types with refs by @dmontagu in [#8526](https://github.com/pydantic/pydantic/pull/8526)
* Support `pydantic.Field(repr=False)` in dataclasses by @tigeryy2 in [#8511](https://github.com/pydantic/pydantic/pull/8511)
* Override `dataclass_transform` behavior for `RootModel` by @Viicos in [#8163](https://github.com/pydantic/pydantic/pull/8163)
* Refactor signature generation for simplicity by @sydney-runkle in [#8572](https://github.com/pydantic/pydantic/pull/8572)
* Fix ordering bug of PlainValidator annotation by @Anvil in [#8567](https://github.com/pydantic/pydantic/pull/8567)
* Fix `exclude_none` for json serialization of `computed_field`s by @sydney-runkle in [pydantic/pydantic-core#1098](https://github.com/pydantic/pydantic-core/pull/1098)
* Support yyyy-MM-DD string for datetimes by @sydney-runkle in [pydantic/pydantic-core#1124](https://github.com/pydantic/pydantic-core/pull/1124)
* Tweak ordering of definitions in generated schemas by @StrawHatDrag0n in [#8583](https://github.com/pydantic/pydantic/pull/8583)

### New Contributors

#### `pydantic`

* @ekeew made their first contribution in [#6874](https://github.com/pydantic/pydantic/pull/6874)
* @lambertsbennett made their first contribution in [#8054](https://github.com/pydantic/pydantic/pull/8054)
* @vincent-hachin-wmx made their first contribution in [#8138](https://github.com/pydantic/pydantic/pull/8138)
* @QuentinSoubeyranAqemia made their first contribution in [#7825](https://github.com/pydantic/pydantic/pull/7825)
* @ariebovenberg made their first contribution in [#8072](https://github.com/pydantic/pydantic/pull/8072)
* @LukeTonin made their first contribution in [#8223](https://github.com/pydantic/pydantic/pull/8223)
* @denisart made their first contribution in [#8231](https://github.com/pydantic/pydantic/pull/8231)
* @ianhfc made their first contribution in [#8066](https://github.com/pydantic/pydantic/pull/8066)
* @eonu made their first contribution in [#8255](https://github.com/pydantic/pydantic/pull/8255)
* @amandahla made their first contribution in [#8263](https://github.com/pydantic/pydantic/pull/8263)
* @ibleedicare made their first contribution in [#8262](https://github.com/pydantic/pydantic/pull/8262)
* @jevins09 made their first contribution in [#8316](https://github.com/pydantic/pydantic/pull/8316)
* @cuu508 made their first contribution in [#8322](https://github.com/pydantic/pydantic/pull/8322)
* @slanzmich made their first contribution in [#8305](https://github.com/pydantic/pydantic/pull/8305)
* @jensenbox made their first contribution in [#8331](https://github.com/pydantic/pydantic/pull/8331)
* @szepeviktor made their first contribution in [#8356](https://github.com/pydantic/pydantic/pull/8356)
* @Elkiwa made their first contribution in [#8341](https://github.com/pydantic/pydantic/pull/8341)
* @parhamfh made their first contribution in [#8395](https://github.com/pydantic/pydantic/pull/8395)
* @shenxiangzhuang made their first contribution in [#8402](https://github.com/pydantic/pydantic/pull/8402)
* @NeevCohen made their first contribution in [#8387](https://github.com/pydantic/pydantic/pull/8387)
* @zby made their first contribution in [#8497](https://github.com/pydantic/pydantic/pull/8497)
* @patelnets made their first contribution in [#8491](https://github.com/pydantic/pydantic/pull/8491)
* @edwardwli made their first contribution in [#8503](https://github.com/pydantic/pydantic/pull/8503)
* @luca-matei made their first contribution in [#8507](https://github.com/pydantic/pydantic/pull/8507)
* @Jocelyn-Gas made their first contribution in [#8437](https://github.com/pydantic/pydantic/pull/8437)
* @bL34cHig0 made their first contribution in [#8501](https://github.com/pydantic/pydantic/pull/8501)
* @tigeryy2 made their first contribution in [#8511](https://github.com/pydantic/pydantic/pull/8511)
* @geospackle made their first contribution in [#8537](https://github.com/pydantic/pydantic/pull/8537)
* @Anvil made their first contribution in [#8567](https://github.com/pydantic/pydantic/pull/8567)
* @hungtsetse made their first contribution in [#8546](https://github.com/pydantic/pydantic/pull/8546)
* @StrawHatDrag0n made their first contribution in [#8583](https://github.com/pydantic/pydantic/pull/8583)

#### `pydantic-core`

* @mariuswinger made their first contribution in [pydantic/pydantic-core#1087](https://github.com/pydantic/pydantic-core/pull/1087)
* @adamchainz made their first contribution in [pydantic/pydantic-core#1090](https://github.com/pydantic/pydantic-core/pull/1090)
* @akx made their first contribution in [pydantic/pydantic-core#1123](https://github.com/pydantic/pydantic-core/pull/1123)

## v2.6.0b1 (2024-01-19)

Pre-release, see [the GitHub release](https://github.com/pydantic/pydantic/releases/tag/v2.6.0b1) for details.

## v2.5.3 (2023-12-22)

[GitHub release](https://github.com/pydantic/pydantic/releases/tag/v2.5.3)

### What's Changed

#### Packaging

* uprev `pydantic-core` to 2.14.6

#### Fixes

* Fix memory leak with recursive definitions creating reference cycles by @davidhewitt in [pydantic/pydantic-core#1125](https://github.com/pydantic/pydantic-core/pull/1125)

## v2.5.2 (2023-11-22)

[GitHub release](https://github.com/pydantic/pydantic/releases/tag/v2.5.2)

### What's Changed

#### Packaging

* uprev `pydantic-core` to 2.14.5

#### New Features

* Add `ConfigDict.ser_json_inf_nan` by @davidhewitt in [#8159](https://github.com/pydantic/pydantic/pull/8159)

#### Fixes

* Fix validation of `Literal` from JSON keys when used as `dict` key by @sydney-runkle in [pydantic/pydantic-core#1075](https://github.com/pydantic/pydantic-core/pull/1075)
* Fix bug re `custom_init` on members of `Union` by @sydney-runkle in [pydantic/pydantic-core#1076](https://github.com/pydantic/pydantic-core/pull/1076)
* Fix `JsonValue` `bool` serialization by @sydney-runkle in [#8190](https://github.com/pydantic/pydantic/pull/8159)
* Fix handling of unhashable inputs with `Literal` in `Union`s by @sydney-runkle in [pydantic/pydantic-core#1089](https://github.com/pydantic/pydantic-core/pull/1089)

## v2.5.1 (2023-11-15)

[GitHub release](https://github.com/pydantic/pydantic/releases/tag/v2.5.1)

### What's Changed

#### Packaging

* uprev pydantic-core to 2.14.3 by @samuelcolvin in [#8120](https://github.com/pydantic/pydantic/pull/8120)

#### Fixes

* Fix package description limit by @dmontagu in [#8097](https://github.com/pydantic/pydantic/pull/8097)
* Fix `ValidateCallWrapper` error when creating a model which has a @validate_call wrapped field annotation by @sydney-runkle in [#8110](https://github.com/pydantic/pydantic/pull/8110)

## v2.5.0 (2023-11-13)

[GitHub release](https://github.com/pydantic/pydantic/releases/tag/v2.5.0)

The code released in v2.5.0 is functionally identical to that of v2.5.0b1.

### What's Changed

#### Packaging

* Update pydantic-core from 2.10.1 to 2.14.1, significant changes from these updates are described below, full changelog [here](https://github.com/pydantic/pydantic-core/compare/v2.10.1...v2.14.1)
* Update to `pyright==1.1.335` by @Viicos in [#8075](https://github.com/pydantic/pydantic/pull/8075)

#### New Features

* Allow plugins to catch non `ValidationError` errors by @adriangb in [#7806](https://github.com/pydantic/pydantic/pull/7806)
* Support `__doc__` argument in `create_model()` by @chris-spann in [#7863](https://github.com/pydantic/pydantic/pull/7863)
* Expose `regex_engine` flag - meaning you can use with the Rust or Python regex libraries in constraints by @utkini in [#7768](https://github.com/pydantic/pydantic/pull/7768)
* Save return type generated from type annotation in `ComputedFieldInfo` by @alexmojaki in [#7889](https://github.com/pydantic/pydantic/pull/7889)
* Adopting `ruff` formatter by @Luca-Blight in [#7930](https://github.com/pydantic/pydantic/pull/7930)
* Added `validation_error_cause` to config by @zakstucke in [#7626](https://github.com/pydantic/pydantic/pull/7626)
* Make path of the item to validate available in plugin by @hramezani in [#7861](https://github.com/pydantic/pydantic/pull/7861)
* Add `CallableDiscriminator` and `Tag` by @dmontagu in [#7983](https://github.com/pydantic/pydantic/pull/7983)
    * `CallableDiscriminator` renamed to `Discriminator` by @dmontagu in [#8047](https://github.com/pydantic/pydantic/pull/8047)
* Make union case tags affect union error messages by @dmontagu in [#8001](https://github.com/pydantic/pydantic/pull/8001)
* Add `examples` and `json_schema_extra` to `@computed_field` by @alexmojaki in [#8013](https://github.com/pydantic/pydantic/pull/8013)
* Add `JsonValue` type by @dmontagu in [#7998](https://github.com/pydantic/pydantic/pull/7998)
* Allow `str` as argument to `Discriminator` by @dmontagu in [#8047](https://github.com/pydantic/pydantic/pull/8047)
* Add `SchemaSerializer.__reduce__` method to enable pickle serialization by @edoakes in [pydantic/pydantic-core#1006](https://github.com/pydantic/pydantic-core/pull/1006)

#### Changes

* **Significant Change:** replace `ultra_strict` with new smart union implementation, the way unions are validated has changed significantly to improve performance and correctness, we have worked hard to absolutely minimise the number of cases where behaviour has changed, see the PR for details - by @davidhewitt in [pydantic/pydantic-core#867](https://github.com/pydantic/pydantic-core/pull/867)
* Add support for instance method reassignment when `extra='allow'` by @sydney-runkle in [#7683](https://github.com/pydantic/pydantic/pull/7683)
* Support JSON schema generation for `Enum` types with no cases by @sydney-runkle in [#7927](https://github.com/pydantic/pydantic/pull/7927)
* Warn if a class inherits from `Generic` before `BaseModel` by @alexmojaki in [#7891](https://github.com/pydantic/pydantic/pull/7891)

#### Performance

* New custom JSON parser, `jiter` by @samuelcolvin in [pydantic/pydantic-core#974](https://github.com/pydantic/pydantic-core/pull/974)
* PGO build for MacOS M1 by @samuelcolvin in [pydantic/pydantic-core#1063](https://github.com/pydantic/pydantic-core/pull/1063)
* Use `__getattr__` for all package imports, improve import time by @samuelcolvin in [#7947](https://github.com/pydantic/pydantic/pull/7947)

#### Fixes

* Fix `mypy` issue with subclasses of `RootModel` by @sydney-runkle in [#7677](https://github.com/pydantic/pydantic/pull/7677)
* Properly rebuild the `FieldInfo` when a forward ref gets evaluated by @dmontagu in [#7698](https://github.com/pydantic/pydantic/pull/7698)
* Fix failure to load `SecretStr` from JSON (regression in v2.4) by @sydney-runkle in [#7729](https://github.com/pydantic/pydantic/pull/7729)
* Fix `defer_build` behavior with `TypeAdapter` by @sydney-runkle in [#7736](https://github.com/pydantic/pydantic/pull/7736)
* Improve compatibility with legacy `mypy` versions by @dmontagu in [#7742](https://github.com/pydantic/pydantic/pull/7742)
* Fix: update `TypeVar` handling when default is not set by @pmmmwh in [#7719](https://github.com/pydantic/pydantic/pull/7719)
* Support specification of `strict` on `Enum` type fields by @sydney-runkle in [#7761](https://github.com/pydantic/pydantic/pull/7761)
* Wrap `weakref.ref` instead of subclassing to fix `cloudpickle` serialization by @edoakes in [#7780](https://github.com/pydantic/pydantic/pull/7780)
* Keep values of private attributes set within `model_post_init` in subclasses by @alexmojaki in [#7775](https://github.com/pydantic/pydantic/pull/7775)
* Add more specific type for non-callable `json_schema_extra` by @alexmojaki in [#7803](https://github.com/pydantic/pydantic/pull/7803)
* Raise an error when deleting frozen (model) fields by @alexmojaki in [#7800](https://github.com/pydantic/pydantic/pull/7800)
* Fix schema sorting bug with default values by @sydney-runkle in [#7817](https://github.com/pydantic/pydantic/pull/7817)
* Use generated alias for aliases that are not specified otherwise by @alexmojaki in [#7802](https://github.com/pydantic/pydantic/pull/7802)
* Support `strict` specification for `UUID` types by @sydney-runkle in [#7865](https://github.com/pydantic/pydantic/pull/7865)
* JSON schema: fix extra parameter handling by @me-and in [#7810](https://github.com/pydantic/pydantic/pull/7810)
* Fix: support `pydantic.Field(kw_only=True)` with inherited dataclasses by @PrettyWood in [#7827](https://github.com/pydantic/pydantic/pull/7827)
* Support `validate_call` decorator for methods in classes with `__slots__` by @sydney-runkle in [#7883](https://github.com/pydantic/pydantic/pull/7883)
* Fix pydantic dataclass problem with `dataclasses.field` default by @hramezani in [#7898](https://github.com/pydantic/pydantic/pull/7898)
* Fix schema generation for generics with union type bounds by @sydney-runkle in [#7899](https://github.com/pydantic/pydantic/pull/7899)
* Fix version for `importlib_metadata` on python 3.7 by @sydney-runkle in [#7904](https://github.com/pydantic/pydantic/pull/7904)
* Support `|` operator (Union) in PydanticRecursiveRef by @alexmojaki in [#7892](https://github.com/pydantic/pydantic/pull/7892)
* Fix `display_as_type` for `TypeAliasType` in python 3.12 by @dmontagu in [#7929](https://github.com/pydantic/pydantic/pull/7929)
* Add support for `NotRequired` generics in `TypedDict` by @sydney-runkle in [#7932](https://github.com/pydantic/pydantic/pull/7932)
* Make generic `TypeAliasType` specifications produce different schema definitions by @alexdrydew in [#7893](https://github.com/pydantic/pydantic/pull/7893)
* Added fix for signature of inherited dataclass by @howsunjow in [#7925](https://github.com/pydantic/pydantic/pull/7925)
* Make the model name generation more robust in JSON schema by @joakimnordling in [#7881](https://github.com/pydantic/pydantic/pull/7881)
* Fix plurals in validation error messages (in tests) by @Iipin in [#7972](https://github.com/pydantic/pydantic/pull/7972)
* `PrivateAttr` is passed from `Annotated` default position by @tabassco in [#8004](https://github.com/pydantic/pydantic/pull/8004)
* Don't decode bytes (which may not be UTF8) when displaying SecretBytes by @alexmojaki in [#8012](https://github.com/pydantic/pydantic/pull/8012)
* Use `classmethod` instead of `classmethod[Any, Any, Any]` by @Mr-Pepe in [#7979](https://github.com/pydantic/pydantic/pull/7979)
* Clearer error on invalid Plugin by @samuelcolvin in [#8023](https://github.com/pydantic/pydantic/pull/8023)
* Correct pydantic dataclasses import by @samuelcolvin in [#8027](https://github.com/pydantic/pydantic/pull/8027)
* Fix misbehavior for models referencing redefined type aliases by @dmontagu in [#8050](https://github.com/pydantic/pydantic/pull/8050)
* Fix `Optional` field with `validate_default` only performing one field validation by @sydney-runkle in [pydantic/pydantic-core#1002](https://github.com/pydantic/pydantic-core/pull/1002)
* Fix `definition-ref` bug with `Dict` keys by @sydney-runkle in [pydantic/pydantic-core#1014](https://github.com/pydantic/pydantic-core/pull/1014)
* Fix bug allowing validation of `bool` types with `coerce_numbers_to_str=True` by @sydney-runkle in [pydantic/pydantic-core#1017](https://github.com/pydantic/pydantic-core/pull/1017)
* Don't accept `NaN` in float and decimal constraints by @davidhewitt in [pydantic/pydantic-core#1037](https://github.com/pydantic/pydantic-core/pull/1037)
* Add `lax_str` and `lax_int` support for enum values not inherited from str/int by @michaelhly in [pydantic/pydantic-core#1015](https://github.com/pydantic/pydantic-core/pull/1015)
* Support subclasses in lists in `Union` of `List` types by @sydney-runkle in [pydantic/pydantic-core#1039](https://github.com/pydantic/pydantic-core/pull/1039)
* Allow validation against `max_digits` and `decimals` to pass if normalized or non-normalized input is valid by @sydney-runkle in [pydantic/pydantic-core#1049](https://github.com/pydantic/pydantic-core/pull/1049)
* Fix: proper pluralization in `ValidationError` messages by @Iipin in [pydantic/pydantic-core#1050](https://github.com/pydantic/pydantic-core/pull/1050)
* Disallow the string `'-'` as `datetime` input by @davidhewitt in [pydantic/speedate#52](https://github.com/pydantic/speedate/pull/52) & [pydantic/pydantic-core#1060](https://github.com/pydantic/pydantic-core/pull/1060)
* Fix: NaN and Inf float serialization by @davidhewitt in [pydantic/pydantic-core#1062](https://github.com/pydantic/pydantic-core/pull/1062)
* Restore manylinux-compatible PGO builds by @davidhewitt in [pydantic/pydantic-core#1068](https://github.com/pydantic/pydantic-core/pull/1068)

### New Contributors

#### `pydantic`

* @schneebuzz made their first contribution in [#7699](https://github.com/pydantic/pydantic/pull/7699)
* @edoakes made their first contribution in [#7780](https://github.com/pydantic/pydantic/pull/7780)
* @alexmojaki made their first contribution in [#7775](https://github.com/pydantic/pydantic/pull/7775)
* @NickG123 made their first contribution in [#7751](https://github.com/pydantic/pydantic/pull/7751)
* @gowthamgts made their first contribution in [#7830](https://github.com/pydantic/pydantic/pull/7830)
* @jamesbraza made their first contribution in [#7848](https://github.com/pydantic/pydantic/pull/7848)
* @laundmo made their first contribution in [#7850](https://github.com/pydantic/pydantic/pull/7850)
* @rahmatnazali made their first contribution in [#7870](https://github.com/pydantic/pydantic/pull/7870)
* @waterfountain1996 made their first contribution in [#7878](https://github.com/pydantic/pydantic/pull/7878)
* @chris-spann made their first contribution in [#7863](https://github.com/pydantic/pydantic/pull/7863)
* @me-and made their first contribution in [#7810](https://github.com/pydantic/pydantic/pull/7810)
* @utkini made their first contribution in [#7768](https://github.com/pydantic/pydantic/pull/7768)
* @bn-l made their first contribution in [#7744](https://github.com/pydantic/pydantic/pull/7744)
* @alexdrydew made their first contribution in [#7893](https://github.com/pydantic/pydantic/pull/7893)
* @Luca-Blight made their first contribution in [#7930](https://github.com/pydantic/pydantic/pull/7930)
* @howsunjow made their first contribution in [#7925](https://github.com/pydantic/pydantic/pull/7925)
* @joakimnordling made their first contribution in [#7881](https://github.com/pydantic/pydantic/pull/7881)
* @icfly2 made their first contribution in [#7976](https://github.com/pydantic/pydantic/pull/7976)
* @Yummy-Yums made their first contribution in [#8003](https://github.com/pydantic/pydantic/pull/8003)
* @Iipin made their first contribution in [#7972](https://github.com/pydantic/pydantic/pull/7972)
* @tabassco made their first contribution in [#8004](https://github.com/pydantic/pydantic/pull/8004)
* @Mr-Pepe made their first contribution in [#7979](https://github.com/pydantic/pydantic/pull/7979)
* @0x00cl made their first contribution in [#8010](https://github.com/pydantic/pydantic/pull/8010)
* @barraponto made their first contribution in [#8032](https://github.com/pydantic/pydantic/pull/8032)

#### `pydantic-core`

* @sisp made their first contribution in [pydantic/pydantic-core#995](https://github.com/pydantic/pydantic-core/pull/995)
* @michaelhly made their first contribution in [pydantic/pydantic-core#1015](https://github.com/pydantic/pydantic-core/pull/1015)

## v2.5.0b1 (2023-11-09)

Pre-release, see [the GitHub release](https://github.com/pydantic/pydantic/releases/tag/v2.5.0b1) for details.

## v2.4.2 (2023-09-27)

[GitHub release](https://github.com/pydantic/pydantic/releases/tag/v2.4.2)

### What's Changed

#### Fixes

* Fix bug with JSON schema for sequence of discriminated union by @dmontagu in [#7647](https://github.com/pydantic/pydantic/pull/7647)
* Fix schema references in discriminated unions by @adriangb in [#7646](https://github.com/pydantic/pydantic/pull/7646)
* Fix json schema generation for recursive models by @adriangb in [#7653](https://github.com/pydantic/pydantic/pull/7653)
* Fix `models_json_schema` for generic models by @adriangb in [#7654](https://github.com/pydantic/pydantic/pull/7654)
* Fix xfailed test for generic model signatures by @adriangb in [#7658](https://github.com/pydantic/pydantic/pull/7658)

### New Contributors

* @austinorr made their first contribution in [#7657](https://github.com/pydantic/pydantic/pull/7657)
* @peterHoburg made their first contribution in [#7670](https://github.com/pydantic/pydantic/pull/7670)

## v2.4.1 (2023-09-26)

[GitHub release](https://github.com/pydantic/pydantic/releases/tag/v2.4.1)

### What's Changed

#### Packaging

* Update pydantic-core to 2.10.1 by @davidhewitt in [#7633](https://github.com/pydantic/pydantic/pull/7633)

#### Fixes

* Serialize unsubstituted type vars as `Any` by @adriangb in [#7606](https://github.com/pydantic/pydantic/pull/7606)
* Remove schema building caches by @adriangb in [#7624](https://github.com/pydantic/pydantic/pull/7624)
* Fix an issue where JSON schema extras weren't JSON encoded by @dmontagu in [#7625](https://github.com/pydantic/pydantic/pull/7625)

## v2.4.0 (2023-09-22)

[GitHub release](https://github.com/pydantic/pydantic/releases/tag/v2.4.0)

### What's Changed

#### Packaging

* Update pydantic-core to 2.10.0 by @samuelcolvin in [#7542](https://github.com/pydantic/pydantic/pull/7542)

#### New Features

* Add `Base64Url` types by @dmontagu in [#7286](https://github.com/pydantic/pydantic/pull/7286)
* Implement optional `number` to `str` coercion by @lig in [#7508](https://github.com/pydantic/pydantic/pull/7508)
* Allow access to `field_name` and `data` in all validators if there is data and a field name by @samuelcolvin in [#7542](https://github.com/pydantic/pydantic/pull/7542)
* Add `BaseModel.model_validate_strings` and `TypeAdapter.validate_strings` by @hramezani in [#7552](https://github.com/pydantic/pydantic/pull/7552)
* Add Pydantic `plugins` experimental implementation by @lig @samuelcolvin and @Kludex in [#6820](https://github.com/pydantic/pydantic/pull/6820)

#### Changes

* Do not override `model_post_init` in subclass with private attrs by @Viicos in [#7302](https://github.com/pydantic/pydantic/pull/7302)
* Make fields with defaults not required in the serialization schema by default by @dmontagu in [#7275](https://github.com/pydantic/pydantic/pull/7275)
* Mark `Extra` as deprecated by @disrupted in [#7299](https://github.com/pydantic/pydantic/pull/7299)
* Make `EncodedStr` a dataclass by @Kludex in [#7396](https://github.com/pydantic/pydantic/pull/7396)
* Move `annotated_handlers` to be public by @samuelcolvin in [#7569](https://github.com/pydantic/pydantic/pull/7569)

#### Performance

* Simplify flattening and inlining of `CoreSchema` by @adriangb in [#7523](https://github.com/pydantic/pydantic/pull/7523)
* Remove unused copies in `CoreSchema` walking by @adriangb in [#7528](https://github.com/pydantic/pydantic/pull/7528)
* Add caches for collecting definitions and invalid schemas from a CoreSchema by @adriangb in [#7527](https://github.com/pydantic/pydantic/pull/7527)
* Eagerly resolve discriminated unions and cache cases where we can't by @adriangb in [#7529](https://github.com/pydantic/pydantic/pull/7529)
* Replace `dict.get` and `dict.setdefault` with more verbose versions in `CoreSchema` building hot paths by @adriangb in [#7536](https://github.com/pydantic/pydantic/pull/7536)
* Cache invalid `CoreSchema` discovery by @adriangb in [#7535](https://github.com/pydantic/pydantic/pull/7535)
* Allow disabling `CoreSchema` validation for faster startup times by @adriangb in [#7565](https://github.com/pydantic/pydantic/pull/7565)

#### Fixes

* Fix config detection for `TypedDict` from grandparent classes by @dmontagu in [#7272](https://github.com/pydantic/pydantic/pull/7272)
* Fix hash function generation for frozen models with unusual MRO by @dmontagu in [#7274](https://github.com/pydantic/pydantic/pull/7274)
* Make `strict` config overridable in field for Path by @hramezani in [#7281](https://github.com/pydantic/pydantic/pull/7281)
* Use `ser_json_<timedelta|bytes>` on default in `GenerateJsonSchema` by @Kludex in [#7269](https://github.com/pydantic/pydantic/pull/7269)
* Adding a check that alias is validated as an identifier for Python by @andree0 in [#7319](https://github.com/pydantic/pydantic/pull/7319)
* Raise an error when computed field overrides field by @sydney-runkle in [#7346](https://github.com/pydantic/pydantic/pull/7346)
* Fix applying `SkipValidation` to referenced schemas by @adriangb in [#7381](https://github.com/pydantic/pydantic/pull/7381)
* Enforce behavior of private attributes having double leading underscore by @lig in [#7265](https://github.com/pydantic/pydantic/pull/7265)
* Standardize `__get_pydantic_core_schema__` signature by @hramezani in [#7415](https://github.com/pydantic/pydantic/pull/7415)
* Fix generic dataclass fields mutation bug (when using `TypeAdapter`) by @sydney-runkle in [#7435](https://github.com/pydantic/pydantic/pull/7435)
* Fix `TypeError` on `model_validator` in `wrap` mode by @pmmmwh in [#7496](https://github.com/pydantic/pydantic/pull/7496)
* Improve enum error message by @hramezani in [#7506](https://github.com/pydantic/pydantic/pull/7506)
* Make `repr` work for instances that failed initialization when handling `ValidationError`s by @dmontagu in [#7439](https://github.com/pydantic/pydantic/pull/7439)
* Fixed a regular expression denial of service issue by limiting whitespaces by @prodigysml in [#7360](https://github.com/pydantic/pydantic/pull/7360)
* Fix handling of `UUID` values having `UUID.version=None` by @lig in [#7566](https://github.com/pydantic/pydantic/pull/7566)
* Fix `__iter__` returning private `cached_property` info by @sydney-runkle in [#7570](https://github.com/pydantic/pydantic/pull/7570)
* Improvements to version info message by @samuelcolvin in [#7594](https://github.com/pydantic/pydantic/pull/7594)

### New Contributors

* @15498th made their first contribution in [#7238](https://github.com/pydantic/pydantic/pull/7238)
* @GabrielCappelli made their first contribution in [#7213](https://github.com/pydantic/pydantic/pull/7213)
* @tobni made their first contribution in [#7184](https://github.com/pydantic/pydantic/pull/7184)
* @redruin1 made their first contribution in [#7282](https://github.com/pydantic/pydantic/pull/7282)
* @FacerAin made their first contribution in [#7288](https://github.com/pydantic/pydantic/pull/7288)
* @acdha made their first contribution in [#7297](https://github.com/pydantic/pydantic/pull/7297)
* @andree0 made their first contribution in [#7319](https://github.com/pydantic/pydantic/pull/7319)
* @gordonhart made their first contribution in [#7375](https://github.com/pydantic/pydantic/pull/7375)
* @pmmmwh made their first contribution in [#7496](https://github.com/pydantic/pydantic/pull/7496)
* @disrupted made their first contribution in [#7299](https://github.com/pydantic/pydantic/pull/7299)
* @prodigysml made their first contribution in [#7360](https://github.com/pydantic/pydantic/pull/7360)

## v2.3.0 (2023-08-23)

[GitHub release](https://github.com/pydantic/pydantic/releases/tag/v2.3.0)

* 🔥 Remove orphaned changes file from repo by @lig in [#7168](https://github.com/pydantic/pydantic/pull/7168)
* Add copy button on documentation by @Kludex in [#7190](https://github.com/pydantic/pydantic/pull/7190)
* Fix docs on JSON type by @Kludex in [#7189](https://github.com/pydantic/pydantic/pull/7189)
* Update mypy 1.5.0 to 1.5.1 in CI by @hramezani in [#7191](https://github.com/pydantic/pydantic/pull/7191)
* fix download links badge by @samuelcolvin in [#7200](https://github.com/pydantic/pydantic/pull/7200)
* add 2.2.1 to changelog by @samuelcolvin in [#7212](https://github.com/pydantic/pydantic/pull/7212)
* Make ModelWrapValidator protocols generic by @dmontagu in [#7154](https://github.com/pydantic/pydantic/pull/7154)
* Correct `Field(..., exclude: bool)` docs by @samuelcolvin in [#7214](https://github.com/pydantic/pydantic/pull/7214)
* Make shadowing attributes a warning instead of an error by @adriangb in [#7193](https://github.com/pydantic/pydantic/pull/7193)
* Document `Base64Str` and `Base64Bytes` by @Kludex in [#7192](https://github.com/pydantic/pydantic/pull/7192)
* Fix `config.defer_build` for serialization first cases by @samuelcolvin in [#7024](https://github.com/pydantic/pydantic/pull/7024)
* clean Model docstrings in JSON Schema by @samuelcolvin in [#7210](https://github.com/pydantic/pydantic/pull/7210)
* fix [#7228](https://github.com/pydantic/pydantic/pull/7228) (typo): docs in `validators.md` to correct `validate_default` kwarg by @lmmx in [#7229](https://github.com/pydantic/pydantic/pull/7229)
* ✅ Implement `tzinfo.fromutc` method for `TzInfo` in `pydantic-core` by @lig in [#7019](https://github.com/pydantic/pydantic/pull/7019)
* Support `__get_validators__` by @hramezani in [#7197](https://github.com/pydantic/pydantic/pull/7197)

## v2.2.1 (2023-08-18)

[GitHub release](https://github.com/pydantic/pydantic/releases/tag/v2.2.1)

* Make `xfail`ing test for root model extra stop `xfail`ing by @dmontagu in [#6937](https://github.com/pydantic/pydantic/pull/6937)
* Optimize recursion detection by stopping on the second visit for the same object by @mciucu in [#7160](https://github.com/pydantic/pydantic/pull/7160)
* fix link in docs by @tlambert03 in [#7166](https://github.com/pydantic/pydantic/pull/7166)
* Replace MiMalloc w/ default allocator by @adriangb in [pydantic/pydantic-core#900](https://github.com/pydantic/pydantic-core/pull/900)
* Bump pydantic-core to 2.6.1 and prepare 2.2.1 release by @adriangb in [#7176](https://github.com/pydantic/pydantic/pull/7176)

## v2.2.0 (2023-08-17)

[GitHub release](https://github.com/pydantic/pydantic/releases/tag/v2.2.0)

* Split "pipx install" setup command into two commands on the documentation site by @nomadmtb in [#6869](https://github.com/pydantic/pydantic/pull/6869)
* Deprecate `Field.include` by @hramezani in [#6852](https://github.com/pydantic/pydantic/pull/6852)
* Fix typo in default factory error msg by @hramezani in [#6880](https://github.com/pydantic/pydantic/pull/6880)
* Simplify handling of typing.Annotated in GenerateSchema by @dmontagu in [#6887](https://github.com/pydantic/pydantic/pull/6887)
* Re-enable fastapi tests in CI by @dmontagu in [#6883](https://github.com/pydantic/pydantic/pull/6883)
* Make it harder to hit collisions with json schema defrefs by @dmontagu in [#6566](https://github.com/pydantic/pydantic/pull/6566)
* Cleaner error for invalid input to `Path` fields by @samuelcolvin in [#6903](https://github.com/pydantic/pydantic/pull/6903)
* :memo: support Coordinate Type by @yezz123 in [#6906](https://github.com/pydantic/pydantic/pull/6906)
* Fix `ForwardRef` wrapper for py 3.10.0 (shim until bpo-45166) by @randomir in [#6919](https://github.com/pydantic/pydantic/pull/6919)
* Fix misbehavior related to copying of RootModel by @dmontagu in [#6918](https://github.com/pydantic/pydantic/pull/6918)
* Fix issue with recursion error caused by ParamSpec by @dmontagu in [#6923](https://github.com/pydantic/pydantic/pull/6923)
* Add section about Constrained classes to the Migration Guide by @Kludex in [#6924](https://github.com/pydantic/pydantic/pull/6924)
* Use `main` branch for badge links by @Viicos in [#6925](https://github.com/pydantic/pydantic/pull/6925)
* Add test for v1/v2 Annotated discrepancy by @carlbordum in [#6926](https://github.com/pydantic/pydantic/pull/6926)
* Make the v1 mypy plugin work with both v1 and v2 by @dmontagu in [#6921](https://github.com/pydantic/pydantic/pull/6921)
* Fix issue where generic models couldn't be parametrized with BaseModel by @dmontagu in [#6933](https://github.com/pydantic/pydantic/pull/6933)
* Remove xfail for discriminated union with alias by @dmontagu in [#6938](https://github.com/pydantic/pydantic/pull/6938)
* add field_serializer to computed_field by @andresliszt in [#6965](https://github.com/pydantic/pydantic/pull/6965)
* Use union_schema with Type[Union[...]] by @JeanArhancet in [#6952](https://github.com/pydantic/pydantic/pull/6952)
* Fix inherited typeddict attributes / config by @adriangb in [#6981](https://github.com/pydantic/pydantic/pull/6981)
* fix dataclass annotated before validator called twice by @davidhewitt in [#6998](https://github.com/pydantic/pydantic/pull/6998)
* Update test-fastapi deselected tests by @hramezani in [#7014](https://github.com/pydantic/pydantic/pull/7014)
* Fix validator doc format by @hramezani in [#7015](https://github.com/pydantic/pydantic/pull/7015)
* Fix typo in docstring of model_json_schema by @AdamVinch-Federated in [#7032](https://github.com/pydantic/pydantic/pull/7032)
* remove unused "type ignores" with pyright by @samuelcolvin in [#7026](https://github.com/pydantic/pydantic/pull/7026)
* Add benchmark representing FastAPI startup time by @adriangb in [#7030](https://github.com/pydantic/pydantic/pull/7030)
* Fix json_encoders for Enum subclasses by @adriangb in [#7029](https://github.com/pydantic/pydantic/pull/7029)
* Update docstring of `ser_json_bytes` regarding base64 encoding by @Viicos in [#7052](https://github.com/pydantic/pydantic/pull/7052)
* Allow `@validate_call` to work on async methods by @adriangb in [#7046](https://github.com/pydantic/pydantic/pull/7046)
* Fix: mypy error with `Settings` and `SettingsConfigDict` by @JeanArhancet in [#7002](https://github.com/pydantic/pydantic/pull/7002)
* Fix some typos (repeated words and it's/its) by @eumiro in [#7063](https://github.com/pydantic/pydantic/pull/7063)
* Fix the typo in docstring by @harunyasar in [#7062](https://github.com/pydantic/pydantic/pull/7062)
* Docs: Fix broken URL in the pydantic-settings package recommendation by @swetjen in [#6995](https://github.com/pydantic/pydantic/pull/6995)
* Handle constraints being applied to schemas that don't accept it by @adriangb in [#6951](https://github.com/pydantic/pydantic/pull/6951)
* Replace almost_equal_floats with math.isclose by @eumiro in [#7082](https://github.com/pydantic/pydantic/pull/7082)
* bump pydantic-core to 2.5.0 by @davidhewitt in [#7077](https://github.com/pydantic/pydantic/pull/7077)
* Add `short_version` and use it in links by @hramezani in [#7115](https://github.com/pydantic/pydantic/pull/7115)
* 📝 Add usage link to `RootModel` by @Kludex in [#7113](https://github.com/pydantic/pydantic/pull/7113)
* Revert "Fix default port for mongosrv DSNs (#6827)" by @Kludex in [#7116](https://github.com/pydantic/pydantic/pull/7116)
<!-- markdownlint-disable-next-line no-space-in-emphasis -->
* Clarify validate_default and _Unset handling in usage docs and migration guide by @benbenbang in [#6950](https://github.com/pydantic/pydantic/pull/6950)
* Tweak documentation of `Field.exclude` by @Viicos in [#7086](https://github.com/pydantic/pydantic/pull/7086)
* Do not require `validate_assignment` to use `Field.frozen` by @Viicos in [#7103](https://github.com/pydantic/pydantic/pull/7103)
* tweaks to `_core_utils` by @samuelcolvin in [#7040](https://github.com/pydantic/pydantic/pull/7040)
* Make DefaultDict working with set by @hramezani in [#7126](https://github.com/pydantic/pydantic/pull/7126)
* Don't always require typing.Generic as a base for partially parametrized models by @dmontagu in [#7119](https://github.com/pydantic/pydantic/pull/7119)
* Fix issue with JSON schema incorrectly using parent class core schema by @dmontagu in [#7020](https://github.com/pydantic/pydantic/pull/7020)
* Fix xfailed test related to TypedDict and alias_generator by @dmontagu in [#6940](https://github.com/pydantic/pydantic/pull/6940)
* Improve error message for NameEmail by @dmontagu in [#6939](https://github.com/pydantic/pydantic/pull/6939)
* Fix generic computed fields by @dmontagu in [#6988](https://github.com/pydantic/pydantic/pull/6988)
* Reflect namedtuple default values during validation by @dmontagu in [#7144](https://github.com/pydantic/pydantic/pull/7144)
* Update dependencies, fix pydantic-core usage, fix CI issues by @dmontagu in [#7150](https://github.com/pydantic/pydantic/pull/7150)
* Add mypy 1.5.0 by @hramezani in [#7118](https://github.com/pydantic/pydantic/pull/7118)
* Handle non-json native enum values by @adriangb in [#7056](https://github.com/pydantic/pydantic/pull/7056)
* document `round_trip` in Json type documentation  by @jc-louis in [#7137](https://github.com/pydantic/pydantic/pull/7137)
* Relax signature checks to better support builtins and C extension functions as validators by @adriangb in [#7101](https://github.com/pydantic/pydantic/pull/7101)
* add union_mode='left_to_right' by @davidhewitt in [#7151](https://github.com/pydantic/pydantic/pull/7151)
* Include an error message hint for inherited ordering by @yvalencia91 in [#7124](https://github.com/pydantic/pydantic/pull/7124)
* Fix one docs link and resolve some warnings for two others by @dmontagu in [#7153](https://github.com/pydantic/pydantic/pull/7153)
* Include Field extra keys name in warning by @hramezani in [#7136](https://github.com/pydantic/pydantic/pull/7136)

## v2.1.1 (2023-07-25)

[GitHub release](https://github.com/pydantic/pydantic/releases/tag/v2.1.1)

* Skip FieldInfo merging when unnecessary by @dmontagu in [#6862](https://github.com/pydantic/pydantic/pull/6862)

## v2.1.0 (2023-07-25)

[GitHub release](https://github.com/pydantic/pydantic/releases/tag/v2.1.0)

* Add `StringConstraints` for use as Annotated metadata by @adriangb in [#6605](https://github.com/pydantic/pydantic/pull/6605)
* Try to fix intermittently failing CI by @adriangb in [#6683](https://github.com/pydantic/pydantic/pull/6683)
* Remove redundant example of optional vs default. by @ehiggs-deliverect in [#6676](https://github.com/pydantic/pydantic/pull/6676)
* Docs update by @samuelcolvin in [#6692](https://github.com/pydantic/pydantic/pull/6692)
* Remove the Validate always section in validator docs by @adriangb in [#6679](https://github.com/pydantic/pydantic/pull/6679)
* Fix recursion error in json schema generation by @adriangb in [#6720](https://github.com/pydantic/pydantic/pull/6720)
* Fix incorrect subclass check for secretstr by @AlexVndnblcke in [#6730](https://github.com/pydantic/pydantic/pull/6730)
* update pdm / pdm lockfile to 2.8.0 by @davidhewitt in [#6714](https://github.com/pydantic/pydantic/pull/6714)
* unpin pdm on more CI jobs by @davidhewitt in [#6755](https://github.com/pydantic/pydantic/pull/6755)
* improve source locations for auxiliary packages in docs by @davidhewitt in [#6749](https://github.com/pydantic/pydantic/pull/6749)
* Assume builtins don't accept an info argument by @adriangb in [#6754](https://github.com/pydantic/pydantic/pull/6754)
* Fix bug where calling `help(BaseModelSubclass)` raises errors by @hramezani in [#6758](https://github.com/pydantic/pydantic/pull/6758)
* Fix mypy plugin handling of `@model_validator(mode="after")` by @ljodal in [#6753](https://github.com/pydantic/pydantic/pull/6753)
* update pydantic-core to 2.3.1 by @davidhewitt in [#6756](https://github.com/pydantic/pydantic/pull/6756)
* Mypy plugin for settings by @hramezani in [#6760](https://github.com/pydantic/pydantic/pull/6760)
* Use `contentSchema` keyword for JSON schema by @dmontagu in [#6715](https://github.com/pydantic/pydantic/pull/6715)
* fast-path checking finite decimals by @davidhewitt in [#6769](https://github.com/pydantic/pydantic/pull/6769)
* Docs update by @samuelcolvin in [#6771](https://github.com/pydantic/pydantic/pull/6771)
* Improve json schema doc by @hramezani in [#6772](https://github.com/pydantic/pydantic/pull/6772)
* Update validator docs by @adriangb in [#6695](https://github.com/pydantic/pydantic/pull/6695)
* Fix typehint for wrap validator by @dmontagu in [#6788](https://github.com/pydantic/pydantic/pull/6788)
* 🐛 Fix validation warning for unions of Literal and other type by @lig in [#6628](https://github.com/pydantic/pydantic/pull/6628)
* Update documentation for generics support in V2 by @tpdorsey in [#6685](https://github.com/pydantic/pydantic/pull/6685)
* add pydantic-core build info to `version_info()` by @samuelcolvin in [#6785](https://github.com/pydantic/pydantic/pull/6785)
* Fix pydantic dataclasses that use slots with default values by @dmontagu in [#6796](https://github.com/pydantic/pydantic/pull/6796)
* Fix inheritance of hash function for frozen models by @dmontagu in [#6789](https://github.com/pydantic/pydantic/pull/6789)
* ✨ Add `SkipJsonSchema` annotation by @Kludex in [#6653](https://github.com/pydantic/pydantic/pull/6653)
* Error if an invalid field name is used with Field by @dmontagu in [#6797](https://github.com/pydantic/pydantic/pull/6797)
* Add `GenericModel` to `MOVED_IN_V2` by @adriangb in [#6776](https://github.com/pydantic/pydantic/pull/6776)
* Remove unused code from `docs/usage/types/custom.md` by @hramezani in [#6803](https://github.com/pydantic/pydantic/pull/6803)
* Fix `float` -> `Decimal` coercion precision loss by @adriangb in [#6810](https://github.com/pydantic/pydantic/pull/6810)
* remove email validation from the north star benchmark by @davidhewitt in [#6816](https://github.com/pydantic/pydantic/pull/6816)
* Fix link to mypy by @progsmile in [#6824](https://github.com/pydantic/pydantic/pull/6824)
* Improve initialization hooks example by @hramezani in [#6822](https://github.com/pydantic/pydantic/pull/6822)
* Fix default port for mongosrv DSNs by @dmontagu in [#6827](https://github.com/pydantic/pydantic/pull/6827)
* Improve API documentation, in particular more links between usage and API docs by @samuelcolvin in [#6780](https://github.com/pydantic/pydantic/pull/6780)
* update pydantic-core to 2.4.0 by @davidhewitt in [#6831](https://github.com/pydantic/pydantic/pull/6831)
* Fix `annotated_types.MaxLen` validator for custom sequence types by @ImogenBits in [#6809](https://github.com/pydantic/pydantic/pull/6809)
* Update V1 by @hramezani in [#6833](https://github.com/pydantic/pydantic/pull/6833)
* Make it so callable JSON schema extra works by @dmontagu in [#6798](https://github.com/pydantic/pydantic/pull/6798)
* Fix serialization issue with `InstanceOf` by @dmontagu in [#6829](https://github.com/pydantic/pydantic/pull/6829)
* Add back support for `json_encoders` by @adriangb in [#6811](https://github.com/pydantic/pydantic/pull/6811)
* Update field annotations when building the schema by @dmontagu in [#6838](https://github.com/pydantic/pydantic/pull/6838)
* Use `WeakValueDictionary` to fix generic memory leak by @dmontagu in [#6681](https://github.com/pydantic/pydantic/pull/6681)
* Add `config.defer_build` to optionally make model building lazy by @samuelcolvin in [#6823](https://github.com/pydantic/pydantic/pull/6823)
* delegate `UUID` serialization to pydantic-core by @davidhewitt in [#6850](https://github.com/pydantic/pydantic/pull/6850)
* Update `json_encoders` docs by @adriangb in [#6848](https://github.com/pydantic/pydantic/pull/6848)
* Fix error message for `staticmethod`/`classmethod` order with validate_call by @dmontagu in [#6686](https://github.com/pydantic/pydantic/pull/6686)
* Improve documentation for `Config` by @samuelcolvin in [#6847](https://github.com/pydantic/pydantic/pull/6847)
* Update serialization doc to mention `Field.exclude` takes priority over call-time `include/exclude` by @hramezani in [#6851](https://github.com/pydantic/pydantic/pull/6851)
* Allow customizing core schema generation by making `GenerateSchema` public by @adriangb in [#6737](https://github.com/pydantic/pydantic/pull/6737)

## v2.0.3 (2023-07-05)

[GitHub release](https://github.com/pydantic/pydantic/releases/tag/v2.0.3)

* Mention PyObject (v1) moving to ImportString (v2) in migration doc by @slafs in [#6456](https://github.com/pydantic/pydantic/pull/6456)
* Fix release-tweet CI by @Kludex in [#6461](https://github.com/pydantic/pydantic/pull/6461)
* Revise the section on required / optional / nullable fields. by @ybressler in [#6468](https://github.com/pydantic/pydantic/pull/6468)
* Warn if a type hint is not in fact a type by @adriangb in [#6479](https://github.com/pydantic/pydantic/pull/6479)
* Replace TransformSchema with GetPydanticSchema by @dmontagu in [#6484](https://github.com/pydantic/pydantic/pull/6484)
* Fix the un-hashability of various annotation types, for use in caching generic containers by @dmontagu in [#6480](https://github.com/pydantic/pydantic/pull/6480)
* PYD-164: Rework custom types docs by @adriangb in [#6490](https://github.com/pydantic/pydantic/pull/6490)
* Fix ci by @adriangb in [#6507](https://github.com/pydantic/pydantic/pull/6507)
* Fix forward ref in generic by @adriangb in [#6511](https://github.com/pydantic/pydantic/pull/6511)
* Fix generation of serialization JSON schemas for core_schema.ChainSchema by @dmontagu in [#6515](https://github.com/pydantic/pydantic/pull/6515)
* Document the change in `Field.alias` behavior in Pydantic V2 by @hramezani in [#6508](https://github.com/pydantic/pydantic/pull/6508)
* Give better error message attempting to compute the json schema of a model with undefined fields by @dmontagu in [#6519](https://github.com/pydantic/pydantic/pull/6519)
* Document `alias_priority` by @tpdorsey in [#6520](https://github.com/pydantic/pydantic/pull/6520)
* Add redirect for types documentation by @tpdorsey in [#6513](https://github.com/pydantic/pydantic/pull/6513)
* Allow updating docs without release by @samuelcolvin in [#6551](https://github.com/pydantic/pydantic/pull/6551)
* Ensure docs tests always run in the right folder by @dmontagu in [#6487](https://github.com/pydantic/pydantic/pull/6487)
* Defer evaluation of return type hints for serializer functions by @dmontagu in [#6516](https://github.com/pydantic/pydantic/pull/6516)
* Disable E501 from Ruff and rely on just Black by @adriangb in [#6552](https://github.com/pydantic/pydantic/pull/6552)
* Update JSON Schema documentation for V2 by @tpdorsey in [#6492](https://github.com/pydantic/pydantic/pull/6492)
* Add documentation of cyclic reference handling by @dmontagu in [#6493](https://github.com/pydantic/pydantic/pull/6493)
* Remove the need for change files by @samuelcolvin in [#6556](https://github.com/pydantic/pydantic/pull/6556)
* add "north star" benchmark by @davidhewitt in [#6547](https://github.com/pydantic/pydantic/pull/6547)
* Update Dataclasses docs by @tpdorsey in [#6470](https://github.com/pydantic/pydantic/pull/6470)
* ♻️ Use different error message on v1 redirects by @Kludex in [#6595](https://github.com/pydantic/pydantic/pull/6595)
* ⬆ Upgrade `pydantic-core` to v2.2.0 by @lig in [#6589](https://github.com/pydantic/pydantic/pull/6589)
* Fix serialization for IPvAny by @dmontagu in [#6572](https://github.com/pydantic/pydantic/pull/6572)
* Improve CI by using PDM instead of pip to install typing-extensions by @adriangb in [#6602](https://github.com/pydantic/pydantic/pull/6602)
* Add `enum` error type docs  by @lig in [#6603](https://github.com/pydantic/pydantic/pull/6603)
* 🐛 Fix `max_length` for unicode strings by @lig in [#6559](https://github.com/pydantic/pydantic/pull/6559)
* Add documentation for accessing features via `pydantic.v1` by @tpdorsey in [#6604](https://github.com/pydantic/pydantic/pull/6604)
* Include extra when iterating over a model by @adriangb in [#6562](https://github.com/pydantic/pydantic/pull/6562)
* Fix typing of model_validator by @adriangb in [#6514](https://github.com/pydantic/pydantic/pull/6514)
* Touch up Decimal validator by @adriangb in [#6327](https://github.com/pydantic/pydantic/pull/6327)
* Fix various docstrings using fixed pytest-examples by @dmontagu in [#6607](https://github.com/pydantic/pydantic/pull/6607)
* Handle function validators in a discriminated union by @dmontagu in [#6570](https://github.com/pydantic/pydantic/pull/6570)
* Review json_schema.md by @tpdorsey in [#6608](https://github.com/pydantic/pydantic/pull/6608)
* Make validate_call work on basemodel methods by @dmontagu in [#6569](https://github.com/pydantic/pydantic/pull/6569)
* add test for big int json serde by @davidhewitt in [#6614](https://github.com/pydantic/pydantic/pull/6614)
* Fix pydantic dataclass problem with dataclasses.field default_factory by @hramezani in [#6616](https://github.com/pydantic/pydantic/pull/6616)
* Fixed mypy type inference for TypeAdapter by @zakstucke in [#6617](https://github.com/pydantic/pydantic/pull/6617)
* Make it work to use None as a generic parameter by @dmontagu in [#6609](https://github.com/pydantic/pydantic/pull/6609)
* Make it work to use `$ref` as an alias by @dmontagu in [#6568](https://github.com/pydantic/pydantic/pull/6568)
* add note to migration guide about changes to `AnyUrl` etc by @davidhewitt in [#6618](https://github.com/pydantic/pydantic/pull/6618)
* 🐛 Support defining `json_schema_extra` on `RootModel` using `Field` by @lig in [#6622](https://github.com/pydantic/pydantic/pull/6622)
* Update pre-commit to prevent commits to main branch on accident by @dmontagu in [#6636](https://github.com/pydantic/pydantic/pull/6636)
* Fix PDM CI for python 3.7 on MacOS/windows by @dmontagu in [#6627](https://github.com/pydantic/pydantic/pull/6627)
* Produce more accurate signatures for pydantic dataclasses by @dmontagu in [#6633](https://github.com/pydantic/pydantic/pull/6633)
* Updates to Url types for Pydantic V2 by @tpdorsey in [#6638](https://github.com/pydantic/pydantic/pull/6638)
* Fix list markdown in `transform` docstring by @StefanBRas in [#6649](https://github.com/pydantic/pydantic/pull/6649)
* simplify slots_dataclass construction to appease mypy by @davidhewitt in [#6639](https://github.com/pydantic/pydantic/pull/6639)
* Update TypedDict schema generation docstring by @adriangb in [#6651](https://github.com/pydantic/pydantic/pull/6651)
* Detect and lint-error for prints by @dmontagu in [#6655](https://github.com/pydantic/pydantic/pull/6655)
* Add xfailing test for pydantic-core PR 766 by @dmontagu in [#6641](https://github.com/pydantic/pydantic/pull/6641)
* Ignore unrecognized fields from dataclasses metadata by @dmontagu in [#6634](https://github.com/pydantic/pydantic/pull/6634)
* Make non-existent class getattr a mypy error by @dmontagu in [#6658](https://github.com/pydantic/pydantic/pull/6658)
* Update pydantic-core to 2.3.0 by @hramezani in [#6648](https://github.com/pydantic/pydantic/pull/6648)
* Use OrderedDict from typing_extensions by @dmontagu in [#6664](https://github.com/pydantic/pydantic/pull/6664)
* Fix typehint for JSON schema extra callable by @dmontagu in [#6659](https://github.com/pydantic/pydantic/pull/6659)

## v2.0.2 (2023-07-05)

[GitHub release](https://github.com/pydantic/pydantic/releases/tag/v2.0.2)

* Fix bug where round-trip pickling/unpickling a `RootModel` would change the value of `__dict__`, [#6457](https://github.com/pydantic/pydantic/pull/6457) by @dmontagu
* Allow single-item discriminated unions, [#6405](https://github.com/pydantic/pydantic/pull/6405) by @dmontagu
* Fix issue with union parsing of enums, [#6440](https://github.com/pydantic/pydantic/pull/6440) by @dmontagu
* Docs: Fixed `constr` documentation, renamed old `regex` to new `pattern`, [#6452](https://github.com/pydantic/pydantic/pull/6452) by @miili
* Change `GenerateJsonSchema.generate_definitions` signature, [#6436](https://github.com/pydantic/pydantic/pull/6436) by @dmontagu

See the full changelog [here](https://github.com/pydantic/pydantic/releases/tag/v2.0.2)

## v2.0.1 (2023-07-04)

[GitHub release](https://github.com/pydantic/pydantic/releases/tag/v2.0.1)

First patch release of Pydantic V2

* Extra fields added via `setattr` (i.e. `m.some_extra_field = 'extra_value'`)
  are added to `.model_extra` if `model_config` `extra='allowed'`. Fixed [#6333](https://github.com/pydantic/pydantic/pull/6333), [#6365](https://github.com/pydantic/pydantic/pull/6365) by @aaraney
* Automatically unpack JSON schema '$ref' for custom types, [#6343](https://github.com/pydantic/pydantic/pull/6343) by @adriangb
* Fix tagged unions multiple processing in submodels, [#6340](https://github.com/pydantic/pydantic/pull/6340) by @suharnikov

See the full changelog [here](https://github.com/pydantic/pydantic/releases/tag/v2.0.1)

## v2.0 (2023-06-30)

[GitHub release](https://github.com/pydantic/pydantic/releases/tag/v2.0)

Pydantic V2 is here! :tada:

See [this post](https://docs.pydantic.dev/2.0/blog/pydantic-v2-final/) for more details.

## v2.0b3 (2023-06-16)

Third beta pre-release of Pydantic V2

See the full changelog [here](https://github.com/pydantic/pydantic/releases/tag/v2.0b3)

## v2.0b2 (2023-06-03)

Add `from_attributes` runtime flag to `TypeAdapter.validate_python` and `BaseModel.model_validate`.

See the full changelog [here](https://github.com/pydantic/pydantic/releases/tag/v2.0b2)

## v2.0b1 (2023-06-01)

First beta pre-release of Pydantic V2

See the full changelog [here](https://github.com/pydantic/pydantic/releases/tag/v2.0b1)

## v2.0a4 (2023-05-05)

Fourth pre-release of Pydantic V2

See the full changelog [here](https://github.com/pydantic/pydantic/releases/tag/v2.0a4)

## v2.0a3 (2023-04-20)

Third pre-release of Pydantic V2

See the full changelog [here](https://github.com/pydantic/pydantic/releases/tag/v2.0a3)

## v2.0a2 (2023-04-12)

Second pre-release of Pydantic V2

See the full changelog [here](https://github.com/pydantic/pydantic/releases/tag/v2.0a2)

## v2.0a1 (2023-04-03)

First pre-release of Pydantic V2!

See [this post](https://docs.pydantic.dev/blog/pydantic-v2-alpha/) for more details.

## v1.10.21 (2025-01-10)

* Fix compatibility with ForwardRef._evaluate and Python < 3.12.4 by @griels in https://github.com/pydantic/pydantic/pull/11232

## v1.10.20 (2025-01-07)

This release provides proper support for Python 3.13, with (Cythonized) wheels published for this version.
As a consequence, Cython was updated from `0.29.x` to `3.0.x`.

* General maintenance of CI and build ecosystem by @Viicos in https://github.com/pydantic/pydantic/pull/10847
    * Update Cython to `3.0.x`.
    * Properly address Python 3.13 deprecation warnings.
    * Migrate packaging to `pyproject.toml`, make use of PEP 517 build options.
    * Use [`build`](https://pypi.org/project/build/) instead of direct `setup.py` invocations.
    * Update various Github Actions versions.
* Replace outdated stpmex link in documentation by @jaredenorris in https://github.com/pydantic/pydantic/pull/10997

## v1.10.19 (2024-11-06)

* Add warning when v2 model is nested in v1 model by @sydney-runkle in https://github.com/pydantic/pydantic/pull/10432
* Fix deprecation warning in V1 `isinstance` check by @alicederyn in https://github.com/pydantic/pydantic/pull/10645

## v1.10.18 (2024-08-22)

* Eval type fix in V1 by @sydney-runkle in https://github.com/pydantic/pydantic/pull/9751
* Add `to_lower_camel` to `__all__` in `utils.py` by @sydney-runkle (direct commit)
* Fix `mypy` v1 plugin for mypy 1.11 release by @flaeppe in https://github.com/pydantic/pydantic/pull/10139
* Fix discriminator key used when discriminator has alias and `.schema(by_alias=False)` by @exs-dwoodward in https://github.com/pydantic/pydantic/pull/10146

## v1.10.17 (2024-06-20)

* Advertise Python 3.12 for 1.10.x! Part Deux by @vfazio in https://github.com/pydantic/pydantic/pull/9644
* Mirrored modules in `v1` namespace to fix typing and object resolution in python>3.11 by @exs-dwoodward in https://github.com/pydantic/pydantic/pull/9660
* setup: remove upper bound from python_requires by @vfazio in https://github.com/pydantic/pydantic/pull/9685

## v1.10.16 (2024-06-11)

* Specify recursive_guard as kwarg in FutureRef._evaluate by @vfazio in https://github.com/pydantic/pydantic/pull/9612
* Fix mypy v1 plugin for upcoming mypy release by @ cdce8p in https://github.com/pydantic/pydantic/pull/9586
* Import modules/objects directly from v1 namespace by @exs-dwoodward in https://github.com/pydantic/pydantic/pull/9162

## v1.10.15 (2024-04-03)

* Add pydantic.v1 namespace to Pydantic v1 by @exs-dmiketa in https://github.com/pydantic/pydantic/pull/9042
* Relax version of typing-extensions for V1 by @SonOfLilit in https://github.com/pydantic/pydantic/pull/8819
* patch fix for mypy by @sydney-runkle in https://github.com/pydantic/pydantic/pull/8765

## v1.10.14 (2024-01-19)

* Update install.md by @dmontagu in #7690
* Fix ci to only deploy docs on release by @sydney-runkle in #7740
* Ubuntu fixes for V1 by @sydney-runkle in #8540 and #8587
* Fix cached_property handling in dataclasses when copied by @rdbisme in #8407

## v1.10.13 (2023-09-27)

* Fix: Add max length check to `pydantic.validate_email`, #7673 by @hramezani
* Docs: Fix pip commands to install v1, #6930 by @chbndrhnns

## v1.10.12 (2023-07-24)

* Fixes the `maxlen` property being dropped on `deque` validation. Happened only if the deque item has been typed. Changes the `_validate_sequence_like` func, [#6581](https://github.com/pydantic/pydantic/pull/6581) by @maciekglowka

## v1.10.11 (2023-07-04)

* Importing create_model in tools.py through relative path instead of absolute path - so that it doesn't import V2 code when copied over to V2 branch, [#6361](https://github.com/pydantic/pydantic/pull/6361) by @SharathHuddar

## v1.10.10 (2023-06-30)

* Add Pydantic `Json` field support to settings management, [#6250](https://github.com/pydantic/pydantic/pull/6250) by @hramezani
* Fixed literal validator errors for unhashable values, [#6188](https://github.com/pydantic/pydantic/pull/6188) by @markus1978
* Fixed bug with generics receiving forward refs, [#6130](https://github.com/pydantic/pydantic/pull/6130) by @mark-todd
* Update install method of FastAPI for internal tests in CI, [#6117](https://github.com/pydantic/pydantic/pull/6117) by @Kludex

## v1.10.9 (2023-06-07)

* Fix trailing zeros not ignored in Decimal validation, [#5968](https://github.com/pydantic/pydantic/pull/5968) by @hramezani
* Fix mypy plugin for v1.4.0, [#5928](https://github.com/pydantic/pydantic/pull/5928) by @cdce8p
* Add future and past date hypothesis strategies, [#5850](https://github.com/pydantic/pydantic/pull/5850) by @bschoenmaeckers
* Discourage usage of Cython 3 with Pydantic 1.x, [#5845](https://github.com/pydantic/pydantic/pull/5845) by @lig

## v1.10.8 (2023-05-23)

* Fix a bug in `Literal` usage with `typing-extension==4.6.0`, [#5826](https://github.com/pydantic/pydantic/pull/5826) by @hramezani
* This solves the (closed) issue [#3849](https://github.com/pydantic/pydantic/pull/3849) where aliased fields that use discriminated union fail to validate when the data contains the non-aliased field name, [#5736](https://github.com/pydantic/pydantic/pull/5736) by @benwah
* Update email-validator dependency to >=2.0.0post2, [#5627](https://github.com/pydantic/pydantic/pull/5627) by @adriangb
* update `AnyClassMethod` for changes in [python/typeshed#9771](https://github.com/python/typeshed/issues/9771), [#5505](https://github.com/pydantic/pydantic/pull/5505) by @ITProKyle

## v1.10.7 (2023-03-22)

* Fix creating schema from model using `ConstrainedStr` with `regex` as dict key, [#5223](https://github.com/pydantic/pydantic/pull/5223) by @matejetz
* Address bug in mypy plugin caused by explicit_package_bases=True, [#5191](https://github.com/pydantic/pydantic/pull/5191) by @dmontagu
* Add implicit defaults in the mypy plugin for Field with no default argument, [#5190](https://github.com/pydantic/pydantic/pull/5190) by @dmontagu
* Fix schema generated for Enum values used as Literals in discriminated unions, [#5188](https://github.com/pydantic/pydantic/pull/5188) by @javibookline
* Fix mypy failures caused by the pydantic mypy plugin when users define `from_orm` in their own classes, [#5187](https://github.com/pydantic/pydantic/pull/5187) by @dmontagu
* Fix `InitVar` usage with pydantic dataclasses, mypy version `1.1.1` and the custom mypy plugin, [#5162](https://github.com/pydantic/pydantic/pull/5162) by @cdce8p

## v1.10.6 (2023-03-08)

* Implement logic to support creating validators from non standard callables by using defaults to identify them and unwrapping `functools.partial` and `functools.partialmethod` when checking the signature, [#5126](https://github.com/pydantic/pydantic/pull/5126) by @JensHeinrich
* Fix mypy plugin for v1.1.1, and fix `dataclass_transform` decorator for pydantic dataclasses, [#5111](https://github.com/pydantic/pydantic/pull/5111) by @cdce8p
* Raise `ValidationError`, not `ConfigError`, when a discriminator value is unhashable, [#4773](https://github.com/pydantic/pydantic/pull/4773) by @kurtmckee

## v1.10.5 (2023-02-15)

* Fix broken parametrized bases handling with `GenericModel`s with complex sets of models, [#5052](https://github.com/pydantic/pydantic/pull/5052) by @MarkusSintonen
* Invalidate mypy cache if plugin config changes, [#5007](https://github.com/pydantic/pydantic/pull/5007) by @cdce8p
* Fix `RecursionError` when deep-copying dataclass types wrapped by pydantic, [#4949](https://github.com/pydantic/pydantic/pull/4949) by @mbillingr
* Fix `X | Y` union syntax breaking `GenericModel`, [#4146](https://github.com/pydantic/pydantic/pull/4146) by @thenx
* Switch coverage badge to show coverage for this branch/release, [#5060](https://github.com/pydantic/pydantic/pull/5060) by @samuelcolvin

## v1.10.4 (2022-12-30)

* Change dependency to `typing-extensions>=4.2.0`, [#4885](https://github.com/pydantic/pydantic/pull/4885) by @samuelcolvin

## v1.10.3 (2022-12-29)

**NOTE: v1.10.3 was ["yanked"](https://pypi.org/help/#yanked) from PyPI due to [#4885](https://github.com/pydantic/pydantic/pull/4885) which is fixed in v1.10.4**

* fix parsing of custom root models, [#4883](https://github.com/pydantic/pydantic/pull/4883) by @gou177
* fix: use dataclass proxy for frozen or empty dataclasses, [#4878](https://github.com/pydantic/pydantic/pull/4878) by @PrettyWood
* Fix `schema` and `schema_json` on models where a model instance is a one of default values, [#4781](https://github.com/pydantic/pydantic/pull/4781) by @Bobronium
* Add Jina AI to sponsors on docs index page, [#4767](https://github.com/pydantic/pydantic/pull/4767) by @samuelcolvin
* fix: support assignment on `DataclassProxy`, [#4695](https://github.com/pydantic/pydantic/pull/4695) by @PrettyWood
* Add `postgresql+psycopg` as allowed scheme for `PostgreDsn` to make it usable with SQLAlchemy 2, [#4689](https://github.com/pydantic/pydantic/pull/4689) by @morian
* Allow dict schemas to have both `patternProperties` and `additionalProperties`, [#4641](https://github.com/pydantic/pydantic/pull/4641) by @jparise
* Fixes error passing None for optional lists with `unique_items`, [#4568](https://github.com/pydantic/pydantic/pull/4568) by @mfulgo
* Fix `GenericModel` with `Callable` param raising a `TypeError`, [#4551](https://github.com/pydantic/pydantic/pull/4551) by @mfulgo
* Fix field regex with `StrictStr` type annotation, [#4538](https://github.com/pydantic/pydantic/pull/4538) by @sisp
* Correct `dataclass_transform` keyword argument name from `field_descriptors` to `field_specifiers`, [#4500](https://github.com/pydantic/pydantic/pull/4500) by @samuelcolvin
* fix: avoid multiple calls of `__post_init__` when dataclasses are inherited, [#4487](https://github.com/pydantic/pydantic/pull/4487) by @PrettyWood
* Reduce the size of binary wheels, [#2276](https://github.com/pydantic/pydantic/pull/2276) by @samuelcolvin

## v1.10.2 (2022-09-05)

* **Revert Change:** Revert percent encoding of URL parts which was originally added in [#4224](https://github.com/pydantic/pydantic/pull/4224), [#4470](https://github.com/pydantic/pydantic/pull/4470) by @samuelcolvin
* Prevent long (length > `4_300`) strings/bytes as input to int fields, see
  [python/cpython#95778](https://github.com/python/cpython/issues/95778) and
  [CVE-2020-10735](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2020-10735), [#1477](https://github.com/pydantic/pydantic/pull/1477) by @samuelcolvin
* fix: dataclass wrapper was not always called, [#4477](https://github.com/pydantic/pydantic/pull/4477) by @PrettyWood
* Use `tomllib` on Python 3.11 when parsing `mypy` configuration, [#4476](https://github.com/pydantic/pydantic/pull/4476) by @hauntsaninja
* Basic fix of `GenericModel` cache to detect order of arguments in `Union` models, [#4474](https://github.com/pydantic/pydantic/pull/4474) by @sveinugu
* Fix mypy plugin when using bare types like `list` and `dict` as `default_factory`, [#4457](https://github.com/pydantic/pydantic/pull/4457) by @samuelcolvin

## v1.10.1 (2022-08-31)

* Add `__hash__` method to `pydantic.color.Color` class, [#4454](https://github.com/pydantic/pydantic/pull/4454) by @czaki

## v1.10.0 (2022-08-30)

* Refactor the whole *pydantic* `dataclass` decorator to really act like its standard lib equivalent.
  It hence keeps `__eq__`, `__hash__`, ... and makes comparison with its non-validated version possible.
  It also fixes usage of `frozen` dataclasses in fields and usage of `default_factory` in nested dataclasses.
  The support of `Config.extra` has been added.
  Finally, config customization directly via a `dict` is now possible, [#2557](https://github.com/pydantic/pydantic/pull/2557) by @PrettyWood
  <br/><br/>
  **BREAKING CHANGES:**
    * The `compiled` boolean (whether *pydantic* is compiled with cython) has been moved from `main.py` to `version.py`
    * Now that `Config.extra` is supported, `dataclass` ignores by default extra arguments (like `BaseModel`)
* Fix PEP487 `__set_name__` protocol in `BaseModel` for PrivateAttrs, [#4407](https://github.com/pydantic/pydantic/pull/4407) by @tlambert03
* Allow for custom parsing of environment variables via `parse_env_var` in `Config`, [#4406](https://github.com/pydantic/pydantic/pull/4406) by @acmiyaguchi
* Rename `master` to `main`, [#4405](https://github.com/pydantic/pydantic/pull/4405) by @hramezani
* Fix `StrictStr` does not raise `ValidationError` when `max_length` is present in `Field`, [#4388](https://github.com/pydantic/pydantic/pull/4388) by @hramezani
* Make `SecretStr` and `SecretBytes` hashable, [#4387](https://github.com/pydantic/pydantic/pull/4387) by @chbndrhnns
* Fix `StrictBytes` does not raise `ValidationError` when `max_length` is present in `Field`, [#4380](https://github.com/pydantic/pydantic/pull/4380) by @JeanArhancet
* Add support for bare `type`, [#4375](https://github.com/pydantic/pydantic/pull/4375) by @hramezani
* Support Python 3.11, including binaries for 3.11 in PyPI, [#4374](https://github.com/pydantic/pydantic/pull/4374) by @samuelcolvin
* Add support for `re.Pattern`, [#4366](https://github.com/pydantic/pydantic/pull/4366) by @hramezani
* Fix `__post_init_post_parse__` is incorrectly passed keyword arguments when no `__post_init__` is defined, [#4361](https://github.com/pydantic/pydantic/pull/4361) by @hramezani
* Fix implicitly importing `ForwardRef` and `Callable` from `pydantic.typing` instead of `typing` and also expose `MappingIntStrAny`, [#4358](https://github.com/pydantic/pydantic/pull/4358) by @aminalaee
* remove `Any` types from the `dataclass` decorator so it can be used with the `disallow_any_expr` mypy option, [#4356](https://github.com/pydantic/pydantic/pull/4356) by @DetachHead
* moved repo to `pydantic/pydantic`, [#4348](https://github.com/pydantic/pydantic/pull/4348) by @yezz123
* fix "extra fields not permitted" error when dataclass with `Extra.forbid` is validated multiple times, [#4343](https://github.com/pydantic/pydantic/pull/4343) by @detachhead
* Add Python 3.9 and 3.10 examples to docs, [#4339](https://github.com/pydantic/pydantic/pull/4339) by @Bobronium
* Discriminated union models now use `oneOf` instead of `anyOf` when generating OpenAPI schema definitions, [#4335](https://github.com/pydantic/pydantic/pull/4335) by @MaxwellPayne
* Allow type checkers to infer inner type of `Json` type. `Json[list[str]]` will be now inferred as `list[str]`,
  `Json[Any]` should be used instead of plain `Json`.
  Runtime behaviour is not changed, [#4332](https://github.com/pydantic/pydantic/pull/4332) by @Bobronium
* Allow empty string aliases by using a `alias is not None` check, rather than `bool(alias)`, [#4253](https://github.com/pydantic/pydantic/pull/4253) by @sergeytsaplin
* Update `ForwardRef`s in `Field.outer_type_`, [#4249](https://github.com/pydantic/pydantic/pull/4249) by @JacobHayes
* The use of `__dataclass_transform__` has been replaced by `typing_extensions.dataclass_transform`, which is the preferred way to mark pydantic models as a dataclass under [PEP 681](https://peps.python.org/pep-0681/), [#4241](https://github.com/pydantic/pydantic/pull/4241) by @multimeric
* Use parent model's `Config` when validating nested `NamedTuple` fields, [#4219](https://github.com/pydantic/pydantic/pull/4219) by @synek
* Update `BaseModel.construct` to work with aliased Fields, [#4192](https://github.com/pydantic/pydantic/pull/4192) by @kylebamos
* Catch certain raised errors in `smart_deepcopy` and revert to `deepcopy` if so, [#4184](https://github.com/pydantic/pydantic/pull/4184) by @coneybeare
* Add `Config.anystr_upper` and `to_upper` kwarg to constr and conbytes, [#4165](https://github.com/pydantic/pydantic/pull/4165) by @satheler
* Fix JSON schema for `set` and `frozenset` when they include default values, [#4155](https://github.com/pydantic/pydantic/pull/4155) by @aminalaee
* Teach the mypy plugin that methods decorated by `@validator` are classmethods, [#4102](https://github.com/pydantic/pydantic/pull/4102) by @DMRobertson
* Improve mypy plugin's ability to detect required fields, [#4086](https://github.com/pydantic/pydantic/pull/4086) by @richardxia
* Support fields of type `Type[]` in schema, [#4051](https://github.com/pydantic/pydantic/pull/4051) by @aminalaee
* Add `default` value in JSON Schema when `const=True`, [#4031](https://github.com/pydantic/pydantic/pull/4031) by @aminalaee
* Adds reserved word check to signature generation logic, [#4011](https://github.com/pydantic/pydantic/pull/4011) by @strue36
* Fix Json strategy failure for the complex nested field, [#4005](https://github.com/pydantic/pydantic/pull/4005) by @sergiosim
* Add JSON-compatible float constraint `allow_inf_nan`, [#3994](https://github.com/pydantic/pydantic/pull/3994) by @tiangolo
* Remove undefined behaviour when `env_prefix` had characters in common with `env_nested_delimiter`, [#3975](https://github.com/pydantic/pydantic/pull/3975) by @arsenron
* Support generics model with `create_model`, [#3945](https://github.com/pydantic/pydantic/pull/3945) by @hot123s
* allow submodels to overwrite extra field info, [#3934](https://github.com/pydantic/pydantic/pull/3934) by @PrettyWood
* Document and test structural pattern matching ([PEP 636](https://peps.python.org/pep-0636/)) on `BaseModel`, [#3920](https://github.com/pydantic/pydantic/pull/3920) by @irgolic
* Fix incorrect deserialization of python timedelta object to ISO 8601 for negative time deltas.
  Minus was serialized in incorrect place ("P-1DT23H59M59.888735S" instead of correct "-P1DT23H59M59.888735S"), [#3899](https://github.com/pydantic/pydantic/pull/3899) by @07pepa
* Fix validation of discriminated union fields with an alias when passing a model instance, [#3846](https://github.com/pydantic/pydantic/pull/3846) by @chornsby
* Add a CockroachDsn type to validate CockroachDB connection strings. The type
  supports the following schemes: `cockroachdb`, `cockroachdb+psycopg2` and `cockroachdb+asyncpg`, [#3839](https://github.com/pydantic/pydantic/pull/3839) by @blubber
* Fix MyPy plugin to not override pre-existing `__init__` method in models, [#3824](https://github.com/pydantic/pydantic/pull/3824) by @patrick91
* Fix mypy version checking, [#3783](https://github.com/pydantic/pydantic/pull/3783) by @KotlinIsland
* support overwriting dunder attributes of `BaseModel` instances, [#3777](https://github.com/pydantic/pydantic/pull/3777) by @PrettyWood
* Added `ConstrainedDate` and `condate`, [#3740](https://github.com/pydantic/pydantic/pull/3740) by @hottwaj
* Support `kw_only` in dataclasses, [#3670](https://github.com/pydantic/pydantic/pull/3670) by @detachhead
* Add comparison method for `Color` class, [#3646](https://github.com/pydantic/pydantic/pull/3646) by @aminalaee
* Drop support for python3.6, associated cleanup, [#3605](https://github.com/pydantic/pydantic/pull/3605) by @samuelcolvin
* created new function `to_lower_camel()` for "non pascal case" camel case, [#3463](https://github.com/pydantic/pydantic/pull/3463) by @schlerp
* Add checks to `default` and `default_factory` arguments in Mypy plugin, [#3430](https://github.com/pydantic/pydantic/pull/3430) by @klaa97
* fix mangling of `inspect.signature` for `BaseModel`, [#3413](https://github.com/pydantic/pydantic/pull/3413) by @fix-inspect-signature
* Adds the `SecretField` abstract class so that all the current and future secret fields like `SecretStr` and `SecretBytes` will derive from it, [#3409](https://github.com/pydantic/pydantic/pull/3409) by @expobrain
* Support multi hosts validation in `PostgresDsn`, [#3337](https://github.com/pydantic/pydantic/pull/3337) by @rglsk
* Fix parsing of very small numeric timedelta values, [#3315](https://github.com/pydantic/pydantic/pull/3315) by @samuelcolvin
* Update `SecretsSettingsSource` to respect `config.case_sensitive`, [#3273](https://github.com/pydantic/pydantic/pull/3273) by @JeanArhancet
* Add MongoDB network data source name (DSN) schema, [#3229](https://github.com/pydantic/pydantic/pull/3229) by @snosratiershad
* Add support for multiple dotenv files, [#3222](https://github.com/pydantic/pydantic/pull/3222) by @rekyungmin
* Raise an explicit `ConfigError` when multiple fields are incorrectly set for a single validator, [#3215](https://github.com/pydantic/pydantic/pull/3215) by @SunsetOrange
* Allow ellipsis on `Field`s inside `Annotated` for `TypedDicts` required, [#3133](https://github.com/pydantic/pydantic/pull/3133) by @ezegomez
* Catch overflow errors in `int_validator`, [#3112](https://github.com/pydantic/pydantic/pull/3112) by @ojii
* Adds a `__rich_repr__` method to `Representation` class which enables pretty printing with [Rich](https://github.com/willmcgugan/rich), [#3099](https://github.com/pydantic/pydantic/pull/3099) by @willmcgugan
* Add percent encoding in `AnyUrl` and descendent types, [#3061](https://github.com/pydantic/pydantic/pull/3061) by @FaresAhmedb
* `validate_arguments` decorator now supports `alias`, [#3019](https://github.com/pydantic/pydantic/pull/3019) by @MAD-py
* Avoid `__dict__` and `__weakref__` attributes in `AnyUrl` and IP address fields, [#2890](https://github.com/pydantic/pydantic/pull/2890) by @nuno-andre
* Add ability to use `Final` in a field type annotation, [#2766](https://github.com/pydantic/pydantic/pull/2766) by @uriyyo
* Update requirement to `typing_extensions>=4.1.0` to guarantee `dataclass_transform` is available, [#4424](https://github.com/pydantic/pydantic/pull/4424) by @commonism
* Add Explosion and AWS to main sponsors, [#4413](https://github.com/pydantic/pydantic/pull/4413) by @samuelcolvin
* Update documentation for `copy_on_model_validation` to reflect recent changes, [#4369](https://github.com/pydantic/pydantic/pull/4369) by @samuelcolvin
* Runtime warning if `__slots__` is passed to `create_model`, `__slots__` is then ignored, [#4432](https://github.com/pydantic/pydantic/pull/4432) by @samuelcolvin
* Add type hints to `BaseSettings.Config` to avoid mypy errors, also correct mypy version compatibility notice in docs, [#4450](https://github.com/pydantic/pydantic/pull/4450) by @samuelcolvin

## v1.10.0b1 (2022-08-24)

Pre-release, see [the GitHub release](https://github.com/pydantic/pydantic/releases/tag/v1.10.0b1) for details.

## v1.10.0a2 (2022-08-24)

Pre-release, see [the GitHub release](https://github.com/pydantic/pydantic/releases/tag/v1.10.0a2) for details.

## v1.10.0a1 (2022-08-22)

Pre-release, see [the GitHub release](https://github.com/pydantic/pydantic/releases/tag/v1.10.0a1) for details.

## v1.9.2 (2022-08-11)

**Revert Breaking Change**: *v1.9.1* introduced a breaking change where model fields were
deep copied by default, this release reverts the default behaviour to match *v1.9.0* and before,
while also allow deep-copy behaviour via `copy_on_model_validation = 'deep'`. See [#4092](https://github.com/pydantic/pydantic/pull/4092) for more information.

* Allow for shallow copies of model fields, `Config.copy_on_model_validation` is now a str which must be
  `'none'`, `'deep'`, or `'shallow'` corresponding to not copying, deep copy & shallow copy; default `'shallow'`,
  [#4093](https://github.com/pydantic/pydantic/pull/4093) by @timkpaine

## v1.9.1 (2022-05-19)

Thank you to pydantic's sponsors:
@tiangolo, @stellargraph, @JonasKs, @grillazz, @Mazyod, @kevinalh, @chdsbd, @povilasb, @povilasb, @jina-ai,
@mainframeindustries, @robusta-dev, @SendCloud, @rszamszur, @jodal, @hardbyte, @corleyma, @daddycocoaman,
@Rehket, @jokull, @reillysiemens, @westonsteimel, @primer-io, @koxudaxi, @browniebroke, @stradivari96,
@adriangb, @kamalgill, @jqueguiner, @dev-zero, @datarootsio, @RedCarpetUp
for their kind support.

* Limit the size of `generics._generic_types_cache` and `generics._assigned_parameters`
  to avoid unlimited increase in memory usage, [#4083](https://github.com/pydantic/pydantic/pull/4083) by @samuelcolvin
* Add Jupyverse and FPS as Jupyter projects using pydantic, [#4082](https://github.com/pydantic/pydantic/pull/4082) by @davidbrochart
* Speedup `__isinstancecheck__` on pydantic models when the type is not a model, may also avoid memory "leaks", [#4081](https://github.com/pydantic/pydantic/pull/4081) by @samuelcolvin
* Fix in-place modification of `FieldInfo` that caused problems with PEP 593 type aliases, [#4067](https://github.com/pydantic/pydantic/pull/4067) by @adriangb
* Add support for autocomplete in VS Code via `__dataclass_transform__` when using `pydantic.dataclasses.dataclass`, [#4006](https://github.com/pydantic/pydantic/pull/4006) by @giuliano-oliveira
* Remove benchmarks from codebase and docs, [#3973](https://github.com/pydantic/pydantic/pull/3973) by @samuelcolvin
* Typing checking with pyright in CI, improve docs on vscode/pylance/pyright, [#3972](https://github.com/pydantic/pydantic/pull/3972) by @samuelcolvin
* Fix nested Python dataclass schema regression, [#3819](https://github.com/pydantic/pydantic/pull/3819) by @himbeles
* Update documentation about lazy evaluation of sources for Settings, [#3806](https://github.com/pydantic/pydantic/pull/3806) by @garyd203
* Prevent subclasses of bytes being converted to bytes, [#3706](https://github.com/pydantic/pydantic/pull/3706) by @samuelcolvin
* Fixed "error checking inheritance of" when using PEP585 and PEP604 type hints, [#3681](https://github.com/pydantic/pydantic/pull/3681) by @aleksul
* Allow self referencing `ClassVar`s in models, [#3679](https://github.com/pydantic/pydantic/pull/3679) by @samuelcolvin
* **Breaking Change, see [#4106](https://github.com/pydantic/pydantic/pull/4106)**: Fix issue with self-referencing dataclass, [#3675](https://github.com/pydantic/pydantic/pull/3675) by @uriyyo
* Include non-standard port numbers in rendered URLs, [#3652](https://github.com/pydantic/pydantic/pull/3652) by @dolfinus
* `Config.copy_on_model_validation` does a deep copy and not a shallow one, [#3641](https://github.com/pydantic/pydantic/pull/3641) by @PrettyWood
* fix: clarify that discriminated unions do not support singletons, [#3636](https://github.com/pydantic/pydantic/pull/3636) by @tommilligan
* Add `read_text(encoding='utf-8')` for `setup.py`, [#3625](https://github.com/pydantic/pydantic/pull/3625) by @hswong3i
* Fix JSON Schema generation for Discriminated Unions within lists, [#3608](https://github.com/pydantic/pydantic/pull/3608) by @samuelcolvin

## v1.9.0 (2021-12-31)

Thank you to pydantic's sponsors:
@sthagen, @timdrijvers, @toinbis, @koxudaxi, @ginomempin, @primer-io, @and-semakin, @westonsteimel, @reillysiemens,
@es3n1n, @jokull, @JonasKs, @Rehket, @corleyma, @daddycocoaman, @hardbyte, @datarootsio, @jodal, @aminalaee, @rafsaf,
@jqueguiner, @chdsbd, @kevinalh, @Mazyod, @grillazz, @JonasKs, @simw, @leynier, @xfenix
for their kind support.

### Highlights

* add Python 3.10 support, [#2885](https://github.com/pydantic/pydantic/pull/2885) by @PrettyWood
* [Discriminated unions](https://docs.pydantic.dev/usage/types/#discriminated-unions-aka-tagged-unions), [#619](https://github.com/pydantic/pydantic/pull/619) by @PrettyWood
* [`Config.smart_union` for better union logic](https://docs.pydantic.dev/usage/model_config/#smart-union), [#2092](https://github.com/pydantic/pydantic/pull/2092) by @PrettyWood
* Binaries for Macos M1 CPUs, [#3498](https://github.com/pydantic/pydantic/pull/3498) by @samuelcolvin
* Complex types can be set via [nested environment variables](https://docs.pydantic.dev/usage/settings/#parsing-environment-variable-values), e.g. `foo___bar`, [#3159](https://github.com/pydantic/pydantic/pull/3159) by @Air-Mark
* add a dark mode to *pydantic* documentation, [#2913](https://github.com/pydantic/pydantic/pull/2913) by @gbdlin
* Add support for autocomplete in VS Code via `__dataclass_transform__`, [#2721](https://github.com/pydantic/pydantic/pull/2721) by @tiangolo
* Add "exclude" as a field parameter so that it can be configured using model config, [#660](https://github.com/pydantic/pydantic/pull/660) by @daviskirk

### v1.9.0 (2021-12-31) Changes

* Apply `update_forward_refs` to `Config.json_encodes` prevent name clashes in types defined via strings, [#3583](https://github.com/pydantic/pydantic/pull/3583) by @samuelcolvin
* Extend pydantic's mypy plugin to support mypy versions `0.910`, `0.920`, `0.921` & `0.930`, [#3573](https://github.com/pydantic/pydantic/pull/3573) & [#3594](https://github.com/pydantic/pydantic/pull/3594) by @PrettyWood, @christianbundy, @samuelcolvin

### v1.9.0a2 (2021-12-24) Changes

* support generic models with discriminated union, [#3551](https://github.com/pydantic/pydantic/pull/3551) by @PrettyWood
* keep old behaviour of `json()` by default, [#3542](https://github.com/pydantic/pydantic/pull/3542) by @PrettyWood
* Removed typing-only `__root__` attribute from `BaseModel`, [#3540](https://github.com/pydantic/pydantic/pull/3540) by @layday
* Build Python 3.10 wheels, [#3539](https://github.com/pydantic/pydantic/pull/3539) by @mbachry
* Fix display of `extra` fields with model `__repr__`, [#3234](https://github.com/pydantic/pydantic/pull/3234) by @cocolman
* models copied via `Config.copy_on_model_validation` always have all fields, [#3201](https://github.com/pydantic/pydantic/pull/3201) by @PrettyWood
* nested ORM from nested dictionaries, [#3182](https://github.com/pydantic/pydantic/pull/3182) by @PrettyWood
* fix link to discriminated union section by @PrettyWood

### v1.9.0a1 (2021-12-18) Changes

* Add support for `Decimal`-specific validation configurations in `Field()`, additionally to using `condecimal()`,
  to allow better support from editors and tooling, [#3507](https://github.com/pydantic/pydantic/pull/3507) by @tiangolo
* Add `arm64` binaries suitable for MacOS with an M1 CPU to PyPI, [#3498](https://github.com/pydantic/pydantic/pull/3498) by @samuelcolvin
* Fix issue where `None` was considered invalid when using a `Union` type containing `Any` or `object`, [#3444](https://github.com/pydantic/pydantic/pull/3444) by @tharradine
* When generating field schema, pass optional `field` argument (of type
  `pydantic.fields.ModelField`) to `__modify_schema__()` if present, [#3434](https://github.com/pydantic/pydantic/pull/3434) by @jasujm
* Fix issue when pydantic fail to parse `typing.ClassVar` string type annotation, [#3401](https://github.com/pydantic/pydantic/pull/3401) by @uriyyo
* Mention Python >= 3.9.2 as an alternative to `typing_extensions.TypedDict`, [#3374](https://github.com/pydantic/pydantic/pull/3374) by @BvB93
* Changed the validator method name in the [Custom Errors example](https://docs.pydantic.dev/usage/models/#custom-errors)
  to more accurately describe what the validator is doing; changed from `name_must_contain_space` to `value_must_equal_bar`, [#3327](https://github.com/pydantic/pydantic/pull/3327) by @michaelrios28
* Add `AmqpDsn` class, [#3254](https://github.com/pydantic/pydantic/pull/3254) by @kludex
* Always use `Enum` value as default in generated JSON schema, [#3190](https://github.com/pydantic/pydantic/pull/3190) by @joaommartins
* Add support for Mypy 0.920, [#3175](https://github.com/pydantic/pydantic/pull/3175) by @christianbundy
* `validate_arguments` now supports `extra` customization (used to always be `Extra.forbid`), [#3161](https://github.com/pydantic/pydantic/pull/3161) by @PrettyWood
* Complex types can be set by nested environment variables, [#3159](https://github.com/pydantic/pydantic/pull/3159) by @Air-Mark
* Fix mypy plugin to collect fields based on `pydantic.utils.is_valid_field` so that it ignores untyped private variables, [#3146](https://github.com/pydantic/pydantic/pull/3146) by @hi-ogawa
* fix `validate_arguments` issue with `Config.validate_all`, [#3135](https://github.com/pydantic/pydantic/pull/3135) by @PrettyWood
* avoid dict coercion when using dict subclasses as field type, [#3122](https://github.com/pydantic/pydantic/pull/3122) by @PrettyWood
* add support for `object` type, [#3062](https://github.com/pydantic/pydantic/pull/3062) by @PrettyWood
* Updates pydantic dataclasses to keep `_special` properties on parent classes, [#3043](https://github.com/pydantic/pydantic/pull/3043) by @zulrang
* Add a `TypedDict` class for error objects, [#3038](https://github.com/pydantic/pydantic/pull/3038) by @matthewhughes934
* Fix support for using a subclass of an annotation as a default, [#3018](https://github.com/pydantic/pydantic/pull/3018) by @JacobHayes
* make `create_model_from_typeddict` mypy compliant, [#3008](https://github.com/pydantic/pydantic/pull/3008) by @PrettyWood
* Make multiple inheritance work when using `PrivateAttr`, [#2989](https://github.com/pydantic/pydantic/pull/2989) by @hmvp
* Parse environment variables as JSON, if they have a `Union` type with a complex subfield, [#2936](https://github.com/pydantic/pydantic/pull/2936) by @cbartz
* Prevent `StrictStr` permitting `Enum` values where the enum inherits from `str`, [#2929](https://github.com/pydantic/pydantic/pull/2929) by @samuelcolvin
* Make `SecretsSettingsSource` parse values being assigned to fields of complex types when sourced from a secrets file,
  just as when sourced from environment variables, [#2917](https://github.com/pydantic/pydantic/pull/2917) by @davidmreed
* add a dark mode to *pydantic* documentation, [#2913](https://github.com/pydantic/pydantic/pull/2913) by @gbdlin
* Make `pydantic-mypy` plugin compatible with `pyproject.toml` configuration, consistent with `mypy` changes.
  See the [doc](https://docs.pydantic.dev/mypy_plugin/#configuring-the-plugin) for more information, [#2908](https://github.com/pydantic/pydantic/pull/2908) by @jrwalk
* add Python 3.10 support, [#2885](https://github.com/pydantic/pydantic/pull/2885) by @PrettyWood
* Correctly parse generic models with `Json[T]`, [#2860](https://github.com/pydantic/pydantic/pull/2860) by @geekingfrog
* Update contrib docs re: Python version to use for building docs, [#2856](https://github.com/pydantic/pydantic/pull/2856) by @paxcodes
* Clarify documentation about *pydantic*'s support for custom validation and strict type checking,
  despite *pydantic* being primarily a parsing library, [#2855](https://github.com/pydantic/pydantic/pull/2855) by @paxcodes
* Fix schema generation for `Deque` fields, [#2810](https://github.com/pydantic/pydantic/pull/2810) by @sergejkozin
* fix an edge case when mixing constraints and `Literal`, [#2794](https://github.com/pydantic/pydantic/pull/2794) by @PrettyWood
* Fix postponed annotation resolution for `NamedTuple` and `TypedDict` when they're used directly as the type of fields
  within Pydantic models, [#2760](https://github.com/pydantic/pydantic/pull/2760) by @jameysharp
* Fix bug when `mypy` plugin fails on `construct` method call for `BaseSettings` derived classes, [#2753](https://github.com/pydantic/pydantic/pull/2753) by @uriyyo
* Add function overloading for a `pydantic.create_model` function, [#2748](https://github.com/pydantic/pydantic/pull/2748) by @uriyyo
* Fix mypy plugin issue with self field declaration, [#2743](https://github.com/pydantic/pydantic/pull/2743) by @uriyyo
* The colon at the end of the line "The fields which were supplied when user was initialised:" suggests that the code following it is related.
  Changed it to a period, [#2733](https://github.com/pydantic/pydantic/pull/2733) by @krisaoe
* Renamed variable `schema` to `schema_` to avoid shadowing of global variable name, [#2724](https://github.com/pydantic/pydantic/pull/2724) by @shahriyarr
* Add support for autocomplete in VS Code via `__dataclass_transform__`, [#2721](https://github.com/pydantic/pydantic/pull/2721) by @tiangolo
* add missing type annotations in `BaseConfig` and handle `max_length = 0`, [#2719](https://github.com/pydantic/pydantic/pull/2719) by @PrettyWood
* Change `orm_mode` checking to allow recursive ORM mode parsing with dicts, [#2718](https://github.com/pydantic/pydantic/pull/2718) by @nuno-andre
* Add episode 313 of the *Talk Python To Me* podcast, where Michael Kennedy and Samuel Colvin discuss Pydantic, to the docs, [#2712](https://github.com/pydantic/pydantic/pull/2712) by @RatulMaharaj
* fix JSON schema generation when a field is of type `NamedTuple` and has a default value, [#2707](https://github.com/pydantic/pydantic/pull/2707) by @PrettyWood
* `Enum` fields now properly support extra kwargs in schema generation, [#2697](https://github.com/pydantic/pydantic/pull/2697) by @sammchardy
* **Breaking Change, see [#3780](https://github.com/pydantic/pydantic/pull/3780)**: Make serialization of referenced pydantic models possible, [#2650](https://github.com/pydantic/pydantic/pull/2650) by @PrettyWood
* Add `uniqueItems` option to `ConstrainedList`, [#2618](https://github.com/pydantic/pydantic/pull/2618) by @nuno-andre
* Try to evaluate forward refs automatically at model creation, [#2588](https://github.com/pydantic/pydantic/pull/2588) by @uriyyo
* Switch docs preview and coverage display to use [smokeshow](https://smokeshow.helpmanual.io/), [#2580](https://github.com/pydantic/pydantic/pull/2580) by @samuelcolvin
* Add `__version__` attribute to pydantic module, [#2572](https://github.com/pydantic/pydantic/pull/2572) by @paxcodes
* Add `postgresql+asyncpg`, `postgresql+pg8000`, `postgresql+psycopg2`, `postgresql+psycopg2cffi`, `postgresql+py-postgresql`
  and `postgresql+pygresql` schemes for `PostgresDsn`, [#2567](https://github.com/pydantic/pydantic/pull/2567) by @postgres-asyncpg
* Enable the Hypothesis plugin to generate a constrained decimal when the `decimal_places` argument is specified, [#2524](https://github.com/pydantic/pydantic/pull/2524) by @cwe5590
* Allow `collections.abc.Callable` to be used as type in Python 3.9, [#2519](https://github.com/pydantic/pydantic/pull/2519) by @daviskirk
* Documentation update how to custom compile pydantic when using pip install, small change in `setup.py`
  to allow for custom CFLAGS when compiling, [#2517](https://github.com/pydantic/pydantic/pull/2517) by @peterroelants
* remove side effect of `default_factory` to run it only once even if `Config.validate_all` is set, [#2515](https://github.com/pydantic/pydantic/pull/2515) by @PrettyWood
* Add lookahead to ip regexes for `AnyUrl` hosts. This allows urls with DNS labels
  looking like IPs to validate as they are perfectly valid host names, [#2512](https://github.com/pydantic/pydantic/pull/2512) by @sbv-csis
* Set `minItems` and `maxItems` in generated JSON schema for fixed-length tuples, [#2497](https://github.com/pydantic/pydantic/pull/2497) by @PrettyWood
* Add `strict` argument to `conbytes`, [#2489](https://github.com/pydantic/pydantic/pull/2489) by @koxudaxi
* Support user defined generic field types in generic models, [#2465](https://github.com/pydantic/pydantic/pull/2465) by @daviskirk
* Add an example and a short explanation of subclassing `GetterDict` to docs, [#2463](https://github.com/pydantic/pydantic/pull/2463) by @nuno-andre
* add `KafkaDsn` type, `HttpUrl` now has default port 80 for http and 443 for https, [#2447](https://github.com/pydantic/pydantic/pull/2447) by @MihanixA
* Add `PastDate` and `FutureDate` types, [#2425](https://github.com/pydantic/pydantic/pull/2425) by @Kludex
* Support generating schema for `Generic` fields with subtypes, [#2375](https://github.com/pydantic/pydantic/pull/2375) by @maximberg
* fix(encoder): serialize `NameEmail` to str, [#2341](https://github.com/pydantic/pydantic/pull/2341) by @alecgerona
* add `Config.smart_union` to prevent coercion in `Union` if possible, see
 [the doc](https://docs.pydantic.dev/usage/model_config/#smart-union) for more information, [#2092](https://github.com/pydantic/pydantic/pull/2092) by @PrettyWood
* Add ability to use `typing.Counter` as a model field type, [#2060](https://github.com/pydantic/pydantic/pull/2060) by @uriyyo
* Add parameterised subclasses to `__bases__` when constructing new parameterised classes, so that `A <: B => A[int] <: B[int]`, [#2007](https://github.com/pydantic/pydantic/pull/2007) by @diabolo-dan
* Create `FileUrl` type that allows URLs that conform to [RFC 8089](https://tools.ietf.org/html/rfc8089#section-2).
  Add `host_required` parameter, which is `True` by default (`AnyUrl` and subclasses), `False` in `RedisDsn`, `FileUrl`, [#1983](https://github.com/pydantic/pydantic/pull/1983) by @vgerak
* add `confrozenset()`, analogous to `conset()` and `conlist()`, [#1897](https://github.com/pydantic/pydantic/pull/1897) by @PrettyWood
* stop calling parent class `root_validator` if overridden, [#1895](https://github.com/pydantic/pydantic/pull/1895) by @PrettyWood
* Add `repr` (defaults to `True`) parameter to `Field`, to hide it from the default representation of the `BaseModel`, [#1831](https://github.com/pydantic/pydantic/pull/1831) by @fnep
* Accept empty query/fragment URL parts, [#1807](https://github.com/pydantic/pydantic/pull/1807) by @xavier

## v1.8.2 (2021-05-11)

!!! warning
    A security vulnerability, level "moderate" is fixed in v1.8.2. Please upgrade **ASAP**.
    See security advisory [CVE-2021-29510](https://github.com/pydantic/pydantic/security/advisories/GHSA-5jqp-qgf6-3pvh)

* **Security fix:** Fix `date` and `datetime` parsing so passing either `'infinity'` or `float('inf')`
  (or their negative values) does not cause an infinite loop,
  see security advisory [CVE-2021-29510](https://github.com/pydantic/pydantic/security/advisories/GHSA-5jqp-qgf6-3pvh)
* fix schema generation with Enum by generating a valid name, [#2575](https://github.com/pydantic/pydantic/pull/2575) by @PrettyWood
* fix JSON schema generation with a `Literal` of an enum member, [#2536](https://github.com/pydantic/pydantic/pull/2536) by @PrettyWood
* Fix bug with configurations declarations that are passed as
  keyword arguments during class creation, [#2532](https://github.com/pydantic/pydantic/pull/2532) by @uriyyo
* Allow passing `json_encoders` in class kwargs, [#2521](https://github.com/pydantic/pydantic/pull/2521) by @layday
* support arbitrary types with custom `__eq__`, [#2483](https://github.com/pydantic/pydantic/pull/2483) by @PrettyWood
* support `Annotated` in `validate_arguments` and in generic models with Python 3.9, [#2483](https://github.com/pydantic/pydantic/pull/2483) by @PrettyWood

## v1.8.1 (2021-03-03)

Bug fixes for regressions and new features from `v1.8`

* allow elements of `Config.field` to update elements of a `Field`, [#2461](https://github.com/pydantic/pydantic/pull/2461) by @samuelcolvin
* fix validation with a `BaseModel` field and a custom root type, [#2449](https://github.com/pydantic/pydantic/pull/2449) by @PrettyWood
* expose `Pattern` encoder to `fastapi`, [#2444](https://github.com/pydantic/pydantic/pull/2444) by @PrettyWood
* enable the Hypothesis plugin to generate a constrained float when the `multiple_of` argument is specified, [#2442](https://github.com/pydantic/pydantic/pull/2442) by @tobi-lipede-oodle
* Avoid `RecursionError` when using some types like `Enum` or `Literal` with generic models, [#2436](https://github.com/pydantic/pydantic/pull/2436) by @PrettyWood
* do not overwrite declared `__hash__` in subclasses of a model, [#2422](https://github.com/pydantic/pydantic/pull/2422) by @PrettyWood
* fix `mypy` complaints on `Path` and `UUID` related custom types, [#2418](https://github.com/pydantic/pydantic/pull/2418) by @PrettyWood
* Support properly variable length tuples of compound types, [#2416](https://github.com/pydantic/pydantic/pull/2416) by @PrettyWood

## v1.8 (2021-02-26)

Thank you to pydantic's sponsors:
@jorgecarleitao, @BCarley, @chdsbd, @tiangolo, @matin, @linusg, @kevinalh, @koxudaxi, @timdrijvers, @mkeen, @meadsteve,
@ginomempin, @primer-io, @and-semakin, @tomthorogood, @AjitZK, @westonsteimel, @Mazyod, @christippett, @CarlosDomingues,
@Kludex, @r-m-n
for their kind support.

### Highlights

* [Hypothesis plugin](https://docs.pydantic.dev/hypothesis_plugin/) for testing, [#2097](https://github.com/pydantic/pydantic/pull/2097) by @Zac-HD
* support for [`NamedTuple` and `TypedDict`](https://docs.pydantic.dev/usage/types/#annotated-types), [#2216](https://github.com/pydantic/pydantic/pull/2216) by @PrettyWood
* Support [`Annotated` hints on model fields](https://docs.pydantic.dev/usage/schema/#typingannotated-fields), [#2147](https://github.com/pydantic/pydantic/pull/2147) by @JacobHayes
* [`frozen` parameter on `Config`](https://docs.pydantic.dev/usage/model_config/) to allow models to be hashed, [#1880](https://github.com/pydantic/pydantic/pull/1880) by @rhuille

### Changes

* **Breaking Change**, remove old deprecation aliases from v1, [#2415](https://github.com/pydantic/pydantic/pull/2415) by @samuelcolvin:
    * remove notes on migrating to v1 in docs
    * remove `Schema` which was replaced by `Field`
    * remove `Config.case_insensitive` which was replaced by `Config.case_sensitive` (default `False`)
    * remove `Config.allow_population_by_alias` which was replaced by `Config.allow_population_by_field_name`
    * remove `model.fields` which was replaced by `model.__fields__`
    * remove `model.to_string()` which was replaced by `str(model)`
    * remove `model.__values__` which was replaced by `model.__dict__`
* **Breaking Change:** always validate only first sublevel items with `each_item`.
  There were indeed some edge cases with some compound types where the validated items were the last sublevel ones, [#1933](https://github.com/pydantic/pydantic/pull/1933) by @PrettyWood
* Update docs extensions to fix local syntax highlighting, [#2400](https://github.com/pydantic/pydantic/pull/2400) by @daviskirk
* fix: allow `utils.lenient_issubclass` to handle `typing.GenericAlias` objects like `list[str]` in Python >= 3.9, [#2399](https://github.com/pydantic/pydantic/pull/2399) by @daviskirk
* Improve field declaration for *pydantic* `dataclass` by allowing the usage of *pydantic* `Field` or `'metadata'` kwarg of `dataclasses.field`, [#2384](https://github.com/pydantic/pydantic/pull/2384) by @PrettyWood
* Making `typing-extensions` a required dependency, [#2368](https://github.com/pydantic/pydantic/pull/2368) by @samuelcolvin
* Make `resolve_annotations` more lenient, allowing for missing modules, [#2363](https://github.com/pydantic/pydantic/pull/2363) by @samuelcolvin
* Allow configuring models through class kwargs, [#2356](https://github.com/pydantic/pydantic/pull/2356) by @Bobronium
* Prevent `Mapping` subclasses from always being coerced to `dict`, [#2325](https://github.com/pydantic/pydantic/pull/2325) by @ofek
* fix: allow `None` for type `Optional[conset / conlist]`, [#2320](https://github.com/pydantic/pydantic/pull/2320) by @PrettyWood
* Support empty tuple type, [#2318](https://github.com/pydantic/pydantic/pull/2318) by @PrettyWood
* fix: `python_requires` metadata to require >=3.6.1, [#2306](https://github.com/pydantic/pydantic/pull/2306) by @hukkinj1
* Properly encode `Decimal` with, or without any decimal places, [#2293](https://github.com/pydantic/pydantic/pull/2293) by @hultner
* fix: update `__fields_set__` in `BaseModel.copy(update=…)`, [#2290](https://github.com/pydantic/pydantic/pull/2290) by @PrettyWood
* fix: keep order of fields with `BaseModel.construct()`, [#2281](https://github.com/pydantic/pydantic/pull/2281) by @PrettyWood
* Support generating schema for Generic fields, [#2262](https://github.com/pydantic/pydantic/pull/2262) by @maximberg
* Fix `validate_decorator` so `**kwargs` doesn't exclude values when the keyword
  has the same name as the `*args` or `**kwargs` names, [#2251](https://github.com/pydantic/pydantic/pull/2251) by @cybojenix
* Prevent overriding positional arguments with keyword arguments in
  `validate_arguments`, as per behaviour with native functions, [#2249](https://github.com/pydantic/pydantic/pull/2249) by @cybojenix
* add documentation for `con*` type functions, [#2242](https://github.com/pydantic/pydantic/pull/2242) by @tayoogunbiyi
* Support custom root type (aka `__root__`) when using `parse_obj()` with nested models, [#2238](https://github.com/pydantic/pydantic/pull/2238) by @PrettyWood
* Support custom root type (aka `__root__`) with `from_orm()`, [#2237](https://github.com/pydantic/pydantic/pull/2237) by @PrettyWood
* ensure cythonized functions are left untouched when creating models, based on [#1944](https://github.com/pydantic/pydantic/pull/1944) by @kollmats, [#2228](https://github.com/pydantic/pydantic/pull/2228) by @samuelcolvin
* Resolve forward refs for stdlib dataclasses converted into *pydantic* ones, [#2220](https://github.com/pydantic/pydantic/pull/2220) by @PrettyWood
* Add support for `NamedTuple` and `TypedDict` types.
  Those two types are now handled and validated when used inside `BaseModel` or *pydantic* `dataclass`.
  Two utils are also added `create_model_from_namedtuple` and `create_model_from_typeddict`, [#2216](https://github.com/pydantic/pydantic/pull/2216) by @PrettyWood
* Do not ignore annotated fields when type is `Union[Type[...], ...]`, [#2213](https://github.com/pydantic/pydantic/pull/2213) by @PrettyWood
* Raise a user-friendly `TypeError` when a `root_validator` does not return a `dict` (e.g. `None`), [#2209](https://github.com/pydantic/pydantic/pull/2209) by @masalim2
* Add a `FrozenSet[str]` type annotation to the `allowed_schemes` argument on the `strict_url` field type, [#2198](https://github.com/pydantic/pydantic/pull/2198) by @Midnighter
* add `allow_mutation` constraint to `Field`, [#2195](https://github.com/pydantic/pydantic/pull/2195) by @sblack-usu
* Allow `Field` with a `default_factory` to be used as an argument to a function
  decorated with `validate_arguments`, [#2176](https://github.com/pydantic/pydantic/pull/2176) by @thomascobb
* Allow non-existent secrets directory by only issuing a warning, [#2175](https://github.com/pydantic/pydantic/pull/2175) by @davidolrik
* fix URL regex to parse fragment without query string, [#2168](https://github.com/pydantic/pydantic/pull/2168) by @andrewmwhite
* fix: ensure to always return one of the values in `Literal` field type, [#2166](https://github.com/pydantic/pydantic/pull/2166) by @PrettyWood
* Support `typing.Annotated` hints on model fields. A `Field` may now be set in the type hint with `Annotated[..., Field(...)`; all other annotations are ignored but still visible with `get_type_hints(..., include_extras=True)`, [#2147](https://github.com/pydantic/pydantic/pull/2147) by @JacobHayes
* Added `StrictBytes` type as well as `strict=False` option to `ConstrainedBytes`, [#2136](https://github.com/pydantic/pydantic/pull/2136) by @rlizzo
* added `Config.anystr_lower` and `to_lower` kwarg to `constr` and `conbytes`, [#2134](https://github.com/pydantic/pydantic/pull/2134) by @tayoogunbiyi
* Support plain `typing.Tuple` type, [#2132](https://github.com/pydantic/pydantic/pull/2132) by @PrettyWood
* Add a bound method `validate` to functions decorated with `validate_arguments`
  to validate parameters without actually calling the function, [#2127](https://github.com/pydantic/pydantic/pull/2127) by @PrettyWood
* Add the ability to customize settings sources (add / disable / change priority order), [#2107](https://github.com/pydantic/pydantic/pull/2107) by @kozlek
* Fix mypy complaints about most custom *pydantic* types, [#2098](https://github.com/pydantic/pydantic/pull/2098) by @PrettyWood
* Add a [Hypothesis](https://hypothesis.readthedocs.io/) plugin for easier [property-based testing](https://increment.com/testing/in-praise-of-property-based-testing/) with Pydantic's custom types - [usage details here](https://docs.pydantic.dev/hypothesis_plugin/), [#2097](https://github.com/pydantic/pydantic/pull/2097) by @Zac-HD
* add validator for `None`, `NoneType` or `Literal[None]`, [#2095](https://github.com/pydantic/pydantic/pull/2095) by @PrettyWood
* Handle properly fields of type `Callable` with a default value, [#2094](https://github.com/pydantic/pydantic/pull/2094) by @PrettyWood
* Updated `create_model` return type annotation to return type which inherits from `__base__` argument, [#2071](https://github.com/pydantic/pydantic/pull/2071) by @uriyyo
* Add merged `json_encoders` inheritance, [#2064](https://github.com/pydantic/pydantic/pull/2064) by @art049
* allow overwriting `ClassVar`s in sub-models without having to re-annotate them, [#2061](https://github.com/pydantic/pydantic/pull/2061) by @layday
* add default encoder for `Pattern` type, [#2045](https://github.com/pydantic/pydantic/pull/2045) by @PrettyWood
* Add `NonNegativeInt`, `NonPositiveInt`, `NonNegativeFloat`, `NonPositiveFloat`, [#1975](https://github.com/pydantic/pydantic/pull/1975) by @mdavis-xyz
* Use % for percentage in string format of colors, [#1960](https://github.com/pydantic/pydantic/pull/1960) by @EdwardBetts
* Fixed issue causing `KeyError` to be raised when building schema from multiple `BaseModel` with the same names declared in separate classes, [#1912](https://github.com/pydantic/pydantic/pull/1912) by @JSextonn
* Add `rediss` (Redis over SSL) protocol to `RedisDsn`
  Allow URLs without `user` part (e.g., `rediss://:pass@localhost`), [#1911](https://github.com/pydantic/pydantic/pull/1911) by @TrDex
* Add a new `frozen` boolean parameter to `Config` (default: `False`).
  Setting `frozen=True` does everything that `allow_mutation=False` does, and also generates a `__hash__()` method for the model. This makes instances of the model potentially hashable if all the attributes are hashable, [#1880](https://github.com/pydantic/pydantic/pull/1880) by @rhuille
* fix schema generation with multiple Enums having the same name, [#1857](https://github.com/pydantic/pydantic/pull/1857) by @PrettyWood
* Added support for 13/19 digits VISA credit cards in `PaymentCardNumber` type, [#1416](https://github.com/pydantic/pydantic/pull/1416) by @AlexanderSov
* fix: prevent `RecursionError` while using recursive `GenericModel`s, [#1370](https://github.com/pydantic/pydantic/pull/1370) by @xppt
* use `enum` for `typing.Literal` in JSON schema, [#1350](https://github.com/pydantic/pydantic/pull/1350) by @PrettyWood
* Fix: some recursive models did not require `update_forward_refs` and silently behaved incorrectly, [#1201](https://github.com/pydantic/pydantic/pull/1201) by @PrettyWood
* Fix bug where generic models with fields where the typevar is nested in another type `a: List[T]` are considered to be concrete. This allows these models to be subclassed and composed as expected, [#947](https://github.com/pydantic/pydantic/pull/947) by @daviskirk
* Add `Config.copy_on_model_validation` flag. When set to `False`, *pydantic* will keep models used as fields
  untouched on validation instead of reconstructing (copying) them, [#265](https://github.com/pydantic/pydantic/pull/265) by @PrettyWood

## v1.7.4 (2021-05-11)

* **Security fix:** Fix `date` and `datetime` parsing so passing either `'infinity'` or `float('inf')`
  (or their negative values) does not cause an infinite loop,
  See security advisory [CVE-2021-29510](https://github.com/pydantic/pydantic/security/advisories/GHSA-5jqp-qgf6-3pvh)

## v1.7.3 (2020-11-30)

Thank you to pydantic's sponsors:
@timdrijvers, @BCarley, @chdsbd, @tiangolo, @matin, @linusg, @kevinalh, @jorgecarleitao, @koxudaxi, @primer-api,
@mkeen, @meadsteve for their kind support.

* fix: set right default value for required (optional) fields, [#2142](https://github.com/pydantic/pydantic/pull/2142) by @PrettyWood
* fix: support `underscore_attrs_are_private` with generic models, [#2138](https://github.com/pydantic/pydantic/pull/2138) by @PrettyWood
* fix: update all modified field values in `root_validator` when `validate_assignment` is on, [#2116](https://github.com/pydantic/pydantic/pull/2116) by @PrettyWood
* Allow pickling of `pydantic.dataclasses.dataclass` dynamically created from a built-in `dataclasses.dataclass`, [#2111](https://github.com/pydantic/pydantic/pull/2111) by @aimestereo
* Fix a regression where Enum fields would not propagate keyword arguments to the schema, [#2109](https://github.com/pydantic/pydantic/pull/2109) by @bm424
* Ignore `__doc__` as private attribute when `Config.underscore_attrs_are_private` is set, [#2090](https://github.com/pydantic/pydantic/pull/2090) by @PrettyWood

## v1.7.2 (2020-11-01)

* fix slow `GenericModel` concrete model creation, allow `GenericModel` concrete name reusing in module, [#2078](https://github.com/pydantic/pydantic/pull/2078) by @Bobronium
* keep the order of the fields when `validate_assignment` is set, [#2073](https://github.com/pydantic/pydantic/pull/2073) by @PrettyWood
* forward all the params of the stdlib `dataclass` when converted into *pydantic* `dataclass`, [#2065](https://github.com/pydantic/pydantic/pull/2065) by @PrettyWood

## v1.7.1 (2020-10-28)

Thank you to pydantic's sponsors:
@timdrijvers, @BCarley, @chdsbd, @tiangolo, @matin, @linusg, @kevinalh, @jorgecarleitao, @koxudaxi, @primer-api, @mkeen
for their kind support.

* fix annotation of `validate_arguments` when passing configuration as argument, [#2055](https://github.com/pydantic/pydantic/pull/2055) by @layday
* Fix mypy assignment error when using `PrivateAttr`, [#2048](https://github.com/pydantic/pydantic/pull/2048) by @aphedges
* fix `underscore_attrs_are_private` causing `TypeError` when overriding `__init__`, [#2047](https://github.com/pydantic/pydantic/pull/2047) by @samuelcolvin
* Fixed regression introduced in v1.7 involving exception handling in field validators when `validate_assignment=True`, [#2044](https://github.com/pydantic/pydantic/pull/2044) by @johnsabath
* fix: *pydantic* `dataclass` can inherit from stdlib `dataclass`
  and `Config.arbitrary_types_allowed` is supported, [#2042](https://github.com/pydantic/pydantic/pull/2042) by @PrettyWood

## v1.7 (2020-10-26)

Thank you to pydantic's sponsors:
@timdrijvers, @BCarley, @chdsbd, @tiangolo, @matin, @linusg, @kevinalh, @jorgecarleitao, @koxudaxi, @primer-api
for their kind support.

### Highlights

* Python 3.9 support, thanks @PrettyWood
* [Private model attributes](https://docs.pydantic.dev/usage/models/#private-model-attributes), thanks @Bobronium
* ["secrets files" support in `BaseSettings`](https://docs.pydantic.dev/usage/settings/#secret-support), thanks @mdgilene
* [convert stdlib dataclasses to pydantic dataclasses and use stdlib dataclasses in models](https://docs.pydantic.dev/usage/dataclasses/#stdlib-dataclasses-and-pydantic-dataclasses), thanks @PrettyWood

### Changes

* **Breaking Change:** remove `__field_defaults__`, add `default_factory` support with `BaseModel.construct`.
  Use `.get_default()` method on fields in `__fields__` attribute instead, [#1732](https://github.com/pydantic/pydantic/pull/1732) by @PrettyWood
* Rearrange CI to run linting as a separate job, split install recipes for different tasks, [#2020](https://github.com/pydantic/pydantic/pull/2020) by @samuelcolvin
* Allows subclasses of generic models to make some, or all, of the superclass's type parameters concrete, while
  also defining new type parameters in the subclass, [#2005](https://github.com/pydantic/pydantic/pull/2005) by @choogeboom
* Call validator with the correct `values` parameter type in `BaseModel.__setattr__`,
  when `validate_assignment = True` in model config, [#1999](https://github.com/pydantic/pydantic/pull/1999) by @me-ransh
* Force `fields.Undefined` to be a singleton object, fixing inherited generic model schemas, [#1981](https://github.com/pydantic/pydantic/pull/1981) by @daviskirk
* Include tests in source distributions, [#1976](https://github.com/pydantic/pydantic/pull/1976) by @sbraz
* Add ability to use `min_length/max_length` constraints with secret types, [#1974](https://github.com/pydantic/pydantic/pull/1974) by @uriyyo
* Also check `root_validators` when `validate_assignment` is on, [#1971](https://github.com/pydantic/pydantic/pull/1971) by @PrettyWood
* Fix const validators not running when custom validators are present, [#1957](https://github.com/pydantic/pydantic/pull/1957) by @hmvp
* add `deque` to field types, [#1935](https://github.com/pydantic/pydantic/pull/1935) by @wozniakty
* add basic support for Python 3.9, [#1832](https://github.com/pydantic/pydantic/pull/1832) by @PrettyWood
* Fix typo in the anchor of exporting_models.md#modelcopy and incorrect description, [#1821](https://github.com/pydantic/pydantic/pull/1821) by @KimMachineGun
* Added ability for `BaseSettings` to read "secret files", [#1820](https://github.com/pydantic/pydantic/pull/1820) by @mdgilene
* add `parse_raw_as` utility function, [#1812](https://github.com/pydantic/pydantic/pull/1812) by @PrettyWood
* Support home directory relative paths for `dotenv` files (e.g. `~/.env`), [#1803](https://github.com/pydantic/pydantic/pull/1803) by @PrettyWood
* Clarify documentation for `parse_file` to show that the argument
  should be a file *path* not a file-like object, [#1794](https://github.com/pydantic/pydantic/pull/1794) by @mdavis-xyz
* Fix false positive from mypy plugin when a class nested within a `BaseModel` is named `Model`, [#1770](https://github.com/pydantic/pydantic/pull/1770) by @selimb
* add basic support of Pattern type in schema generation, [#1767](https://github.com/pydantic/pydantic/pull/1767) by @PrettyWood
* Support custom title, description and default in schema of enums, [#1748](https://github.com/pydantic/pydantic/pull/1748) by @PrettyWood
* Properly represent `Literal` Enums when `use_enum_values` is True, [#1747](https://github.com/pydantic/pydantic/pull/1747) by @noelevans
* Allows timezone information to be added to strings to be formatted as time objects. Permitted formats are `Z` for UTC
  or an offset for absolute positive or negative time shifts. Or the timezone data can be omitted, [#1744](https://github.com/pydantic/pydantic/pull/1744) by @noelevans
* Add stub `__init__` with Python 3.6 signature for `ForwardRef`, [#1738](https://github.com/pydantic/pydantic/pull/1738) by @sirtelemak
* Fix behaviour with forward refs and optional fields in nested models, [#1736](https://github.com/pydantic/pydantic/pull/1736) by @PrettyWood
* add `Enum` and `IntEnum` as valid types for fields, [#1735](https://github.com/pydantic/pydantic/pull/1735) by @PrettyWood
* Change default value of `__module__` argument of `create_model` from `None` to `'pydantic.main'`.
  Set reference of created concrete model to it's module to allow pickling (not applied to models created in
  functions), [#1686](https://github.com/pydantic/pydantic/pull/1686) by @Bobronium
* Add private attributes support, [#1679](https://github.com/pydantic/pydantic/pull/1679) by @Bobronium
* add `config` to `@validate_arguments`, [#1663](https://github.com/pydantic/pydantic/pull/1663) by @samuelcolvin
* Allow descendant Settings models to override env variable names for the fields defined in parent Settings models with
  `env` in their `Config`. Previously only `env_prefix` configuration option was applicable, [#1561](https://github.com/pydantic/pydantic/pull/1561) by @ojomio
* Support `ref_template` when creating schema `$ref`s, [#1479](https://github.com/pydantic/pydantic/pull/1479) by @kilo59
* Add a `__call__` stub to `PyObject` so that mypy will know that it is callable, [#1352](https://github.com/pydantic/pydantic/pull/1352) by @brianmaissy
* `pydantic.dataclasses.dataclass` decorator now supports built-in `dataclasses.dataclass`.
  It is hence possible to convert an existing `dataclass` easily to add Pydantic validation.
  Moreover nested dataclasses are also supported, [#744](https://github.com/pydantic/pydantic/pull/744) by @PrettyWood

## v1.6.2 (2021-05-11)

* **Security fix:** Fix `date` and `datetime` parsing so passing either `'infinity'` or `float('inf')`
  (or their negative values) does not cause an infinite loop,
  See security advisory [CVE-2021-29510](https://github.com/pydantic/pydantic/security/advisories/GHSA-5jqp-qgf6-3pvh)

## v1.6.1 (2020-07-15)

* fix validation and parsing of nested models with `default_factory`, [#1710](https://github.com/pydantic/pydantic/pull/1710) by @PrettyWood

## v1.6 (2020-07-11)

Thank you to pydantic's sponsors: @matin, @tiangolo, @chdsbd, @jorgecarleitao, and 1 anonymous sponsor for their kind support.

* Modify validators for `conlist` and `conset` to not have `always=True`, [#1682](https://github.com/pydantic/pydantic/pull/1682) by @samuelcolvin
* add port check to `AnyUrl` (can't exceed 65536) ports are 16 unsigned bits: `0 <= port <= 2**16-1` src: [rfc793 header format](https://tools.ietf.org/html/rfc793#section-3.1), [#1654](https://github.com/pydantic/pydantic/pull/1654) by @flapili
* Document default `regex` anchoring semantics, [#1648](https://github.com/pydantic/pydantic/pull/1648) by @yurikhan
* Use `chain.from_iterable` in class_validators.py. This is a faster and more idiomatic way of using `itertools.chain`.
  Instead of computing all the items in the iterable and storing them in memory, they are computed one-by-one and never
  stored as a huge list. This can save on both runtime and memory space, [#1642](https://github.com/pydantic/pydantic/pull/1642) by @cool-RR
* Add `conset()`, analogous to `conlist()`, [#1623](https://github.com/pydantic/pydantic/pull/1623) by @patrickkwang
* make Pydantic errors (un)pickable, [#1616](https://github.com/pydantic/pydantic/pull/1616) by @PrettyWood
* Allow custom encoding for `dotenv` files, [#1615](https://github.com/pydantic/pydantic/pull/1615) by @PrettyWood
* Ensure `SchemaExtraCallable` is always defined to get type hints on BaseConfig, [#1614](https://github.com/pydantic/pydantic/pull/1614) by @PrettyWood
* Update datetime parser to support negative timestamps, [#1600](https://github.com/pydantic/pydantic/pull/1600) by @mlbiche
* Update mypy, remove `AnyType` alias for `Type[Any]`, [#1598](https://github.com/pydantic/pydantic/pull/1598) by @samuelcolvin
* Adjust handling of root validators so that errors are aggregated from *all* failing root validators, instead of reporting on only the first root validator to fail, [#1586](https://github.com/pydantic/pydantic/pull/1586) by @beezee
* Make `__modify_schema__` on Enums apply to the enum schema rather than fields that use the enum, [#1581](https://github.com/pydantic/pydantic/pull/1581) by @therefromhere
* Fix behavior of `__all__` key when used in conjunction with index keys in advanced include/exclude of fields that are sequences, [#1579](https://github.com/pydantic/pydantic/pull/1579) by @xspirus
* Subclass validators do not run when referencing a `List` field defined in a parent class when `each_item=True`. Added an example to the docs illustrating this, [#1566](https://github.com/pydantic/pydantic/pull/1566) by @samueldeklund
* change `schema.field_class_to_schema` to support `frozenset` in schema, [#1557](https://github.com/pydantic/pydantic/pull/1557) by @wangpeibao
* Call `__modify_schema__` only for the field schema, [#1552](https://github.com/pydantic/pydantic/pull/1552) by @PrettyWood
* Move the assignment of `field.validate_always` in `fields.py` so the `always` parameter of validators work on inheritance, [#1545](https://github.com/pydantic/pydantic/pull/1545) by @dcHHH
* Added support for UUID instantiation through 16 byte strings such as `b'\x12\x34\x56\x78' * 4`. This was done to support `BINARY(16)` columns in sqlalchemy, [#1541](https://github.com/pydantic/pydantic/pull/1541) by @shawnwall
* Add a test assertion that `default_factory` can return a singleton, [#1523](https://github.com/pydantic/pydantic/pull/1523) by @therefromhere
* Add `NameEmail.__eq__` so duplicate `NameEmail` instances are evaluated as equal, [#1514](https://github.com/pydantic/pydantic/pull/1514) by @stephen-bunn
* Add datamodel-code-generator link in pydantic document site, [#1500](https://github.com/pydantic/pydantic/pull/1500) by @koxudaxi
* Added a "Discussion of Pydantic" section to the documentation, with a link to "Pydantic Introduction" video by Alexander Hultnér, [#1499](https://github.com/pydantic/pydantic/pull/1499) by @hultner
* Avoid some side effects of `default_factory` by calling it only once
  if possible and by not setting a default value in the schema, [#1491](https://github.com/pydantic/pydantic/pull/1491) by @PrettyWood
* Added docs about dumping dataclasses to JSON, [#1487](https://github.com/pydantic/pydantic/pull/1487) by @mikegrima
* Make `BaseModel.__signature__` class-only, so getting `__signature__` from model instance will raise `AttributeError`, [#1466](https://github.com/pydantic/pydantic/pull/1466) by @Bobronium
* include `'format': 'password'` in the schema for secret types, [#1424](https://github.com/pydantic/pydantic/pull/1424) by @atheuz
* Modify schema constraints on `ConstrainedFloat` so that `exclusiveMinimum` and
  minimum are not included in the schema if they are equal to `-math.inf` and
  `exclusiveMaximum` and `maximum` are not included if they are equal to `math.inf`, [#1417](https://github.com/pydantic/pydantic/pull/1417) by @vdwees
* Squash internal `__root__` dicts in `.dict()` (and, by extension, in `.json()`), [#1414](https://github.com/pydantic/pydantic/pull/1414) by @patrickkwang
* Move `const` validator to post-validators so it validates the parsed value, [#1410](https://github.com/pydantic/pydantic/pull/1410) by @selimb
* Fix model validation to handle nested literals, e.g. `Literal['foo', Literal['bar']]`, [#1364](https://github.com/pydantic/pydantic/pull/1364) by @DBCerigo
* Remove `user_required = True` from `RedisDsn`, neither user nor password are required, [#1275](https://github.com/pydantic/pydantic/pull/1275) by @samuelcolvin
* Remove extra `allOf` from schema for fields with `Union` and custom `Field`, [#1209](https://github.com/pydantic/pydantic/pull/1209) by @mostaphaRoudsari
* Updates OpenAPI schema generation to output all enums as separate models.
  Instead of inlining the enum values in the model schema, models now use a `$ref`
  property to point to the enum definition, [#1173](https://github.com/pydantic/pydantic/pull/1173) by @calvinwyoung

## v1.5.1 (2020-04-23)

* Signature generation with `extra: allow` never uses a field name, [#1418](https://github.com/pydantic/pydantic/pull/1418) by @prettywood
* Avoid mutating `Field` default value, [#1412](https://github.com/pydantic/pydantic/pull/1412) by @prettywood

## v1.5 (2020-04-18)

* Make includes/excludes arguments for `.dict()`, `._iter()`, ..., immutable, [#1404](https://github.com/pydantic/pydantic/pull/1404) by @AlexECX
* Always use a field's real name with includes/excludes in `model._iter()`, regardless of `by_alias`, [#1397](https://github.com/pydantic/pydantic/pull/1397) by @AlexECX
* Update constr regex example to include start and end lines, [#1396](https://github.com/pydantic/pydantic/pull/1396) by @lmcnearney
* Confirm that shallow `model.copy()` does make a shallow copy of attributes, [#1383](https://github.com/pydantic/pydantic/pull/1383) by @samuelcolvin
* Renaming `model_name` argument of `main.create_model()` to `__model_name` to allow using `model_name` as a field name, [#1367](https://github.com/pydantic/pydantic/pull/1367) by @kittipatv
* Replace raising of exception to silent passing  for non-Var attributes in mypy plugin, [#1345](https://github.com/pydantic/pydantic/pull/1345) by @b0g3r
* Remove `typing_extensions` dependency for Python 3.8, [#1342](https://github.com/pydantic/pydantic/pull/1342) by @prettywood
* Make `SecretStr` and `SecretBytes` initialization idempotent, [#1330](https://github.com/pydantic/pydantic/pull/1330) by @atheuz
* document making secret types dumpable using the json method, [#1328](https://github.com/pydantic/pydantic/pull/1328) by @atheuz
* Move all testing and build to github actions, add windows and macos binaries,
  thank you @StephenBrown2 for much help, [#1326](https://github.com/pydantic/pydantic/pull/1326) by @samuelcolvin
* fix card number length check in `PaymentCardNumber`, `PaymentCardBrand` now inherits from `str`, [#1317](https://github.com/pydantic/pydantic/pull/1317) by @samuelcolvin
* Have `BaseModel` inherit from `Representation` to make mypy happy when overriding `__str__`, [#1310](https://github.com/pydantic/pydantic/pull/1310) by @FuegoFro
* Allow `None` as input to all optional list fields, [#1307](https://github.com/pydantic/pydantic/pull/1307) by @prettywood
* Add `datetime` field to `default_factory` example, [#1301](https://github.com/pydantic/pydantic/pull/1301) by @StephenBrown2
* Allow subclasses of known types to be encoded with superclass encoder, [#1291](https://github.com/pydantic/pydantic/pull/1291) by @StephenBrown2
* Exclude exported fields from all elements of a list/tuple of submodels/dicts with `'__all__'`, [#1286](https://github.com/pydantic/pydantic/pull/1286) by @masalim2
* Add pydantic.color.Color objects as available input for Color fields, [#1258](https://github.com/pydantic/pydantic/pull/1258) by @leosussan
* In examples, type nullable fields as `Optional`, so that these are valid mypy annotations, [#1248](https://github.com/pydantic/pydantic/pull/1248) by @kokes
* Make `pattern_validator()` accept pre-compiled `Pattern` objects. Fix `str_validator()` return type to `str`, [#1237](https://github.com/pydantic/pydantic/pull/1237) by @adamgreg
* Document how to manage Generics and inheritance, [#1229](https://github.com/pydantic/pydantic/pull/1229) by @esadruhn
* `update_forward_refs()` method of BaseModel now copies `__dict__` of class module instead of modifying it, [#1228](https://github.com/pydantic/pydantic/pull/1228) by @paul-ilyin
* Support instance methods and class methods with `@validate_arguments`, [#1222](https://github.com/pydantic/pydantic/pull/1222) by @samuelcolvin
* Add `default_factory` argument to `Field` to create a dynamic default value by passing a zero-argument callable, [#1210](https://github.com/pydantic/pydantic/pull/1210) by @prettywood
* add support for `NewType` of `List`, `Optional`, etc, [#1207](https://github.com/pydantic/pydantic/pull/1207) by @Kazy
* fix mypy signature for `root_validator`, [#1192](https://github.com/pydantic/pydantic/pull/1192) by @samuelcolvin
* Fixed parsing of nested 'custom root type' models, [#1190](https://github.com/pydantic/pydantic/pull/1190) by @Shados
* Add `validate_arguments` function decorator which checks the arguments to a function matches type annotations, [#1179](https://github.com/pydantic/pydantic/pull/1179) by @samuelcolvin
* Add `__signature__` to models, [#1034](https://github.com/pydantic/pydantic/pull/1034) by @Bobronium
* Refactor `._iter()` method, 10x speed boost for `dict(model)`, [#1017](https://github.com/pydantic/pydantic/pull/1017) by @Bobronium

## v1.4 (2020-01-24)

* **Breaking Change:** alias precedence logic changed so aliases on a field always take priority over
  an alias from `alias_generator` to avoid buggy/unexpected behaviour,
  see [here](https://docs.pydantic.dev/usage/model_config/#alias-precedence) for details, [#1178](https://github.com/pydantic/pydantic/pull/1178) by @samuelcolvin
* Add support for unicode and punycode in TLDs, [#1182](https://github.com/pydantic/pydantic/pull/1182) by @jamescurtin
* Fix `cls` argument in validators during assignment, [#1172](https://github.com/pydantic/pydantic/pull/1172) by @samuelcolvin
* completing Luhn algorithm for `PaymentCardNumber`, [#1166](https://github.com/pydantic/pydantic/pull/1166) by @cuencandres
* add support for generics that implement `__get_validators__` like a custom data type, [#1159](https://github.com/pydantic/pydantic/pull/1159) by @tiangolo
* add support for infinite generators with `Iterable`, [#1152](https://github.com/pydantic/pydantic/pull/1152) by @tiangolo
* fix `url_regex` to accept schemas with `+`, `-` and `.` after the first character, [#1142](https://github.com/pydantic/pydantic/pull/1142) by @samuelcolvin
* move `version_info()` to `version.py`, suggest its use in issues, [#1138](https://github.com/pydantic/pydantic/pull/1138) by @samuelcolvin
* Improve pydantic import time by roughly 50% by deferring some module loading and regex compilation, [#1127](https://github.com/pydantic/pydantic/pull/1127) by @samuelcolvin
* Fix `EmailStr` and `NameEmail` to accept instances of themselves in cython, [#1126](https://github.com/pydantic/pydantic/pull/1126) by @koxudaxi
* Pass model class to the `Config.schema_extra` callable, [#1125](https://github.com/pydantic/pydantic/pull/1125) by @therefromhere
* Fix regex for username and password in URLs, [#1115](https://github.com/pydantic/pydantic/pull/1115) by @samuelcolvin
* Add support for nested generic models, [#1104](https://github.com/pydantic/pydantic/pull/1104) by @dmontagu
* add `__all__` to `__init__.py` to prevent "implicit reexport" errors from mypy, [#1072](https://github.com/pydantic/pydantic/pull/1072) by @samuelcolvin
* Add support for using "dotenv" files with `BaseSettings`, [#1011](https://github.com/pydantic/pydantic/pull/1011) by @acnebs

## v1.3 (2019-12-21)

* Change `schema` and `schema_model` to handle dataclasses by using their `__pydantic_model__` feature, [#792](https://github.com/pydantic/pydantic/pull/792) by @aviramha
* Added option for `root_validator` to be skipped if values validation fails using keyword `skip_on_failure=True`, [#1049](https://github.com/pydantic/pydantic/pull/1049) by @aviramha
* Allow `Config.schema_extra` to be a callable so that the generated schema can be post-processed, [#1054](https://github.com/pydantic/pydantic/pull/1054) by @selimb
* Update mypy to version 0.750, [#1057](https://github.com/pydantic/pydantic/pull/1057) by @dmontagu
* Trick Cython into allowing str subclassing, [#1061](https://github.com/pydantic/pydantic/pull/1061) by @skewty
* Prevent type attributes being added to schema unless the attribute `__schema_attributes__` is `True`, [#1064](https://github.com/pydantic/pydantic/pull/1064) by @samuelcolvin
* Change `BaseModel.parse_file` to use `Config.json_loads`, [#1067](https://github.com/pydantic/pydantic/pull/1067) by @kierandarcy
* Fix for optional `Json` fields, [#1073](https://github.com/pydantic/pydantic/pull/1073) by @volker48
* Change the default number of threads used when compiling with cython to one,
  allow override via the `CYTHON_NTHREADS` environment variable, [#1074](https://github.com/pydantic/pydantic/pull/1074) by @samuelcolvin
* Run FastAPI tests during Pydantic's CI tests, [#1075](https://github.com/pydantic/pydantic/pull/1075) by @tiangolo
* My mypy strictness constraints, and associated tweaks to type annotations, [#1077](https://github.com/pydantic/pydantic/pull/1077) by @samuelcolvin
* Add `__eq__` to SecretStr and SecretBytes to allow "value equals", [#1079](https://github.com/pydantic/pydantic/pull/1079) by @sbv-trueenergy
* Fix schema generation for nested None case, [#1088](https://github.com/pydantic/pydantic/pull/1088) by @lutostag
* Consistent checks for sequence like objects, [#1090](https://github.com/pydantic/pydantic/pull/1090) by @samuelcolvin
* Fix `Config` inheritance on `BaseSettings` when used with `env_prefix`, [#1091](https://github.com/pydantic/pydantic/pull/1091) by @samuelcolvin
* Fix for `__modify_schema__` when it conflicted with `field_class_to_schema*`, [#1102](https://github.com/pydantic/pydantic/pull/1102) by @samuelcolvin
* docs: Fix explanation of case sensitive environment variable names when populating `BaseSettings` subclass attributes, [#1105](https://github.com/pydantic/pydantic/pull/1105) by @tribals
* Rename django-rest-framework benchmark in documentation, [#1119](https://github.com/pydantic/pydantic/pull/1119) by @frankie567

## v1.2 (2019-11-28)

* **Possible Breaking Change:** Add support for required `Optional` with `name: Optional[AnyType] = Field(...)`
  and refactor `ModelField` creation to preserve `required` parameter value, [#1031](https://github.com/pydantic/pydantic/pull/1031) by @tiangolo;
  see [here](https://docs.pydantic.dev/usage/models/#required-optional-fields) for details
* Add benchmarks for `cattrs`, [#513](https://github.com/pydantic/pydantic/pull/513) by @sebastianmika
* Add `exclude_none` option to `dict()` and friends, [#587](https://github.com/pydantic/pydantic/pull/587) by @niknetniko
* Add benchmarks for `valideer`, [#670](https://github.com/pydantic/pydantic/pull/670) by @gsakkis
* Add `parse_obj_as` and `parse_file_as` functions for ad-hoc parsing of data into arbitrary pydantic-compatible types, [#934](https://github.com/pydantic/pydantic/pull/934) by @dmontagu
* Add `allow_reuse` argument to validators, thus allowing validator reuse, [#940](https://github.com/pydantic/pydantic/pull/940) by @dmontagu
* Add support for mapping types for custom root models, [#958](https://github.com/pydantic/pydantic/pull/958) by @dmontagu
* Mypy plugin support for dataclasses, [#966](https://github.com/pydantic/pydantic/pull/966) by @koxudaxi
* Add support for dataclasses default factory, [#968](https://github.com/pydantic/pydantic/pull/968) by @ahirner
* Add a `ByteSize` type for converting byte string (`1GB`) to plain bytes, [#977](https://github.com/pydantic/pydantic/pull/977) by @dgasmith
* Fix mypy complaint about `@root_validator(pre=True)`, [#984](https://github.com/pydantic/pydantic/pull/984) by @samuelcolvin
* Add manylinux binaries for Python 3.8 to pypi, also support manylinux2010, [#994](https://github.com/pydantic/pydantic/pull/994) by @samuelcolvin
* Adds ByteSize conversion to another unit, [#995](https://github.com/pydantic/pydantic/pull/995) by @dgasmith
* Fix `__str__` and `__repr__` inheritance for models, [#1022](https://github.com/pydantic/pydantic/pull/1022) by @samuelcolvin
* add testimonials section to docs, [#1025](https://github.com/pydantic/pydantic/pull/1025) by @sullivancolin
* Add support for `typing.Literal` for Python 3.8, [#1026](https://github.com/pydantic/pydantic/pull/1026) by @dmontagu

## v1.1.1 (2019-11-20)

* Fix bug where use of complex fields on sub-models could cause fields to be incorrectly configured, [#1015](https://github.com/pydantic/pydantic/pull/1015) by @samuelcolvin

## v1.1 (2019-11-07)

* Add a mypy plugin for type checking `BaseModel.__init__` and more, [#722](https://github.com/pydantic/pydantic/pull/722) by @dmontagu
* Change return type typehint for `GenericModel.__class_getitem__` to prevent PyCharm warnings, [#936](https://github.com/pydantic/pydantic/pull/936) by @dmontagu
* Fix usage of `Any` to allow `None`, also support `TypeVar` thus allowing use of un-parameterised collection types
  e.g. `Dict` and `List`, [#962](https://github.com/pydantic/pydantic/pull/962) by @samuelcolvin
* Set `FieldInfo` on subfields to fix schema generation for complex nested types, [#965](https://github.com/pydantic/pydantic/pull/965) by @samuelcolvin

## v1.0 (2019-10-23)

* **Breaking Change:** deprecate the `Model.fields` property, use `Model.__fields__` instead, [#883](https://github.com/pydantic/pydantic/pull/883) by @samuelcolvin
* **Breaking Change:** Change the precedence of aliases so child model aliases override parent aliases,
  including using `alias_generator`, [#904](https://github.com/pydantic/pydantic/pull/904) by @samuelcolvin
* **Breaking change:** Rename `skip_defaults` to `exclude_unset`, and add ability to exclude actual defaults, [#915](https://github.com/pydantic/pydantic/pull/915) by @dmontagu
* Add `**kwargs` to `pydantic.main.ModelMetaclass.__new__` so `__init_subclass__` can take custom parameters on extended
  `BaseModel` classes, [#867](https://github.com/pydantic/pydantic/pull/867) by @retnikt
* Fix field of a type that has a default value, [#880](https://github.com/pydantic/pydantic/pull/880) by @koxudaxi
* Use `FutureWarning` instead of `DeprecationWarning` when `alias` instead of `env` is used for settings models, [#881](https://github.com/pydantic/pydantic/pull/881) by @samuelcolvin
* Fix issue with `BaseSettings` inheritance and `alias` getting set to `None`, [#882](https://github.com/pydantic/pydantic/pull/882) by @samuelcolvin
* Modify `__repr__` and `__str__` methods to be consistent across all public classes, add `__pretty__` to support
  python-devtools, [#884](https://github.com/pydantic/pydantic/pull/884) by @samuelcolvin
* deprecation warning for `case_insensitive` on `BaseSettings` config, [#885](https://github.com/pydantic/pydantic/pull/885) by @samuelcolvin
* For `BaseSettings` merge environment variables and in-code values recursively, as long as they create a valid object
  when merged together, to allow splitting init arguments, [#888](https://github.com/pydantic/pydantic/pull/888) by @idmitrievsky
* change secret types example, [#890](https://github.com/pydantic/pydantic/pull/890) by @ashears
* Change the signature of `Model.construct()` to be more user-friendly, document `construct()` usage, [#898](https://github.com/pydantic/pydantic/pull/898) by @samuelcolvin
* Add example for the `construct()` method, [#907](https://github.com/pydantic/pydantic/pull/907) by @ashears
* Improve use of `Field` constraints on complex types, raise an error if constraints are not enforceable,
  also support tuples with an ellipsis `Tuple[X, ...]`, `Sequence` and `FrozenSet` in schema, [#909](https://github.com/pydantic/pydantic/pull/909) by @samuelcolvin
* update docs for bool missing valid value, [#911](https://github.com/pydantic/pydantic/pull/911) by @trim21
* Better `str`/`repr` logic for `ModelField`, [#912](https://github.com/pydantic/pydantic/pull/912) by @samuelcolvin
* Fix `ConstrainedList`, update schema generation to reflect `min_items` and `max_items` `Field()` arguments, [#917](https://github.com/pydantic/pydantic/pull/917) by @samuelcolvin
* Allow abstracts sets (eg. dict keys) in the `include` and `exclude` arguments of `dict()`, [#921](https://github.com/pydantic/pydantic/pull/921) by @samuelcolvin
* Fix JSON serialization errors on `ValidationError.json()` by using `pydantic_encoder`, [#922](https://github.com/pydantic/pydantic/pull/922) by @samuelcolvin
* Clarify usage of `remove_untouched`, improve error message for types with no validators, [#926](https://github.com/pydantic/pydantic/pull/926) by @retnikt

## v1.0b2 (2019-10-07)

* Mark `StrictBool` typecheck as `bool` to allow for default values without mypy errors, [#690](https://github.com/pydantic/pydantic/pull/690) by @dmontagu
* Transfer the documentation build from sphinx to mkdocs, re-write much of the documentation, [#856](https://github.com/pydantic/pydantic/pull/856) by @samuelcolvin
* Add support for custom naming schemes for `GenericModel` subclasses, [#859](https://github.com/pydantic/pydantic/pull/859) by @dmontagu
* Add `if TYPE_CHECKING:` to the excluded lines for test coverage, [#874](https://github.com/pydantic/pydantic/pull/874) by @dmontagu
* Rename `allow_population_by_alias` to `allow_population_by_field_name`, remove unnecessary warning about it, [#875](https://github.com/pydantic/pydantic/pull/875) by @samuelcolvin

## v1.0b1 (2019-10-01)

* **Breaking Change:** rename `Schema` to `Field`, make it a function to placate mypy, [#577](https://github.com/pydantic/pydantic/pull/577) by @samuelcolvin
* **Breaking Change:** modify parsing behavior for `bool`, [#617](https://github.com/pydantic/pydantic/pull/617) by @dmontagu
* **Breaking Change:** `get_validators` is no longer recognised, use `__get_validators__`.
  `Config.ignore_extra` and `Config.allow_extra` are no longer recognised, use `Config.extra`, [#720](https://github.com/pydantic/pydantic/pull/720) by @samuelcolvin
* **Breaking Change:** modify default config settings for `BaseSettings`; `case_insensitive` renamed to `case_sensitive`,
  default changed to `case_sensitive = False`, `env_prefix` default changed to `''` - e.g. no prefix, [#721](https://github.com/pydantic/pydantic/pull/721) by @dmontagu
* **Breaking change:** Implement `root_validator` and rename root errors from `__obj__` to `__root__`, [#729](https://github.com/pydantic/pydantic/pull/729) by @samuelcolvin
* **Breaking Change:** alter the behaviour of `dict(model)` so that sub-models are nolonger
  converted to dictionaries, [#733](https://github.com/pydantic/pydantic/pull/733) by @samuelcolvin
* **Breaking change:** Added `initvars` support to `post_init_post_parse`, [#748](https://github.com/pydantic/pydantic/pull/748) by @Raphael-C-Almeida
* **Breaking Change:** Make `BaseModel.json()` only serialize the `__root__` key for models with custom root, [#752](https://github.com/pydantic/pydantic/pull/752) by @dmontagu
* **Breaking Change:** complete rewrite of `URL` parsing logic, [#755](https://github.com/pydantic/pydantic/pull/755) by @samuelcolvin
* **Breaking Change:** preserve superclass annotations for field-determination when not provided in subclass, [#757](https://github.com/pydantic/pydantic/pull/757) by @dmontagu
* **Breaking Change:** `BaseSettings` now uses the special `env` settings to define which environment variables to
  read, not aliases, [#847](https://github.com/pydantic/pydantic/pull/847) by @samuelcolvin
* add support for `assert` statements inside validators, [#653](https://github.com/pydantic/pydantic/pull/653) by @abdusco
* Update documentation to specify the use of `pydantic.dataclasses.dataclass` and subclassing `pydantic.BaseModel`, [#710](https://github.com/pydantic/pydantic/pull/710) by @maddosaurus
* Allow custom JSON decoding and encoding via `json_loads` and `json_dumps` `Config` properties, [#714](https://github.com/pydantic/pydantic/pull/714) by @samuelcolvin
* make all annotated fields occur in the order declared, [#715](https://github.com/pydantic/pydantic/pull/715) by @dmontagu
* use pytest to test `mypy` integration, [#735](https://github.com/pydantic/pydantic/pull/735) by @dmontagu
* add `__repr__` method to `ErrorWrapper`, [#738](https://github.com/pydantic/pydantic/pull/738) by @samuelcolvin
* Added support for `FrozenSet` members in dataclasses, and a better error when attempting to use types from the `typing` module that are not supported by Pydantic, [#745](https://github.com/pydantic/pydantic/pull/745) by @djpetti
* add documentation for Pycharm Plugin, [#750](https://github.com/pydantic/pydantic/pull/750) by @koxudaxi
* fix broken examples in the docs, [#753](https://github.com/pydantic/pydantic/pull/753) by @dmontagu
* moving typing related objects into `pydantic.typing`, [#761](https://github.com/pydantic/pydantic/pull/761) by @samuelcolvin
* Minor performance improvements to `ErrorWrapper`, `ValidationError` and datetime parsing, [#763](https://github.com/pydantic/pydantic/pull/763) by @samuelcolvin
* Improvements to `datetime`/`date`/`time`/`timedelta` types: more descriptive errors,
  change errors to `value_error` not `type_error`, support bytes, [#766](https://github.com/pydantic/pydantic/pull/766) by @samuelcolvin
* fix error messages for `Literal` types with multiple allowed values, [#770](https://github.com/pydantic/pydantic/pull/770) by @dmontagu
* Improved auto-generated `title` field in JSON schema by converting underscore to space, [#772](https://github.com/pydantic/pydantic/pull/772) by @skewty
* support `mypy --no-implicit-reexport` for dataclasses, also respect `--no-implicit-reexport` in pydantic itself, [#783](https://github.com/pydantic/pydantic/pull/783) by @samuelcolvin
* add the `PaymentCardNumber` type, [#790](https://github.com/pydantic/pydantic/pull/790) by @matin
* Fix const validations for lists, [#794](https://github.com/pydantic/pydantic/pull/794) by @hmvp
* Set `additionalProperties` to false in schema for models with extra fields disallowed, [#796](https://github.com/pydantic/pydantic/pull/796) by @Code0x58
* `EmailStr` validation method now returns local part case-sensitive per RFC 5321, [#798](https://github.com/pydantic/pydantic/pull/798) by @henriklindgren
* Added ability to validate strictness to `ConstrainedFloat`, `ConstrainedInt` and `ConstrainedStr` and added
  `StrictFloat` and `StrictInt` classes, [#799](https://github.com/pydantic/pydantic/pull/799) by @DerRidda
* Improve handling of `None` and `Optional`, replace `whole` with `each_item` (inverse meaning, default `False`)
  on validators, [#803](https://github.com/pydantic/pydantic/pull/803) by @samuelcolvin
* add support for `Type[T]` type hints, [#807](https://github.com/pydantic/pydantic/pull/807) by @timonbimon
* Performance improvements from removing `change_exceptions`, change how pydantic error are constructed, [#819](https://github.com/pydantic/pydantic/pull/819) by @samuelcolvin
* Fix the error message arising when a `BaseModel`-type model field causes a `ValidationError` during parsing, [#820](https://github.com/pydantic/pydantic/pull/820) by @dmontagu
* allow `getter_dict` on `Config`, modify `GetterDict` to be more like a `Mapping` object and thus easier to work with, [#821](https://github.com/pydantic/pydantic/pull/821) by @samuelcolvin
* Only check `TypeVar` param on base `GenericModel` class, [#842](https://github.com/pydantic/pydantic/pull/842) by @zpencerq
* rename `Model._schema_cache` -> `Model.__schema_cache__`, `Model._json_encoder` -> `Model.__json_encoder__`,
  `Model._custom_root_type` -> `Model.__custom_root_type__`, [#851](https://github.com/pydantic/pydantic/pull/851) by @samuelcolvin

## v0.32.2 (2019-08-17)

(Docs are available [here](https://5d584fcca7c9b70007d1c997--pydantic-docs.netlify.com))

* fix `__post_init__` usage with dataclass inheritance, fix [#739](https://github.com/pydantic/pydantic/pull/739) by @samuelcolvin
* fix required fields validation on GenericModels classes, [#742](https://github.com/pydantic/pydantic/pull/742) by @amitbl
* fix defining custom `Schema` on `GenericModel` fields, [#754](https://github.com/pydantic/pydantic/pull/754) by @amitbl

## v0.32.1 (2019-08-08)

* do not validate extra fields when `validate_assignment` is on, [#724](https://github.com/pydantic/pydantic/pull/724) by @YaraslauZhylko

## v0.32 (2019-08-06)

* add model name to `ValidationError` error message, [#676](https://github.com/pydantic/pydantic/pull/676) by @dmontagu
* **breaking change**: remove `__getattr__` and rename `__values__` to `__dict__` on `BaseModel`,
  deprecation warning on use `__values__` attr, attributes access speed increased up to 14 times, [#712](https://github.com/pydantic/pydantic/pull/712) by @Bobronium
* support `ForwardRef` (without self-referencing annotations) in Python 3.6, [#706](https://github.com/pydantic/pydantic/pull/706) by @koxudaxi
* implement `schema_extra` in `Config` sub-class, [#663](https://github.com/pydantic/pydantic/pull/663) by @tiangolo

## v0.31.1 (2019-07-31)

* fix json generation for `EnumError`, [#697](https://github.com/pydantic/pydantic/pull/697) by @dmontagu
* update numerous dependencies

## v0.31 (2019-07-24)

* better support for floating point `multiple_of` values, [#652](https://github.com/pydantic/pydantic/pull/652) by @justindujardin
* fix schema generation for `NewType` and `Literal`, [#649](https://github.com/pydantic/pydantic/pull/649) by @dmontagu
* fix `alias_generator` and field config conflict, [#645](https://github.com/pydantic/pydantic/pull/645) by @gmetzker and [#658](https://github.com/pydantic/pydantic/pull/658) by @Bobronium
* more detailed message for `EnumError`, [#673](https://github.com/pydantic/pydantic/pull/673) by @dmontagu
* add advanced exclude support for `dict`, `json` and `copy`, [#648](https://github.com/pydantic/pydantic/pull/648) by @Bobronium
* fix bug in `GenericModel` for models with concrete parameterized fields, [#672](https://github.com/pydantic/pydantic/pull/672) by @dmontagu
* add documentation for `Literal` type, [#651](https://github.com/pydantic/pydantic/pull/651) by @dmontagu
* add `Config.keep_untouched` for custom descriptors support, [#679](https://github.com/pydantic/pydantic/pull/679) by @Bobronium
* use `inspect.cleandoc` internally to get model description, [#657](https://github.com/pydantic/pydantic/pull/657) by @tiangolo
* add `Color` to schema generation, by @euri10
* add documentation for Literal type, [#651](https://github.com/pydantic/pydantic/pull/651) by @dmontagu

## v0.30.1 (2019-07-15)

* fix so nested classes which inherit and change `__init__` are correctly processed while still allowing `self` as a
  parameter, [#644](https://github.com/pydantic/pydantic/pull/644) by @lnaden and @dgasmith

## v0.30 (2019-07-07)

* enforce single quotes in code, [#612](https://github.com/pydantic/pydantic/pull/612) by @samuelcolvin
* fix infinite recursion with dataclass inheritance and `__post_init__`, [#606](https://github.com/pydantic/pydantic/pull/606) by @Hanaasagi
* fix default values for `GenericModel`, [#610](https://github.com/pydantic/pydantic/pull/610) by @dmontagu
* clarify that self-referencing models require Python 3.7+, [#616](https://github.com/pydantic/pydantic/pull/616) by @vlcinsky
* fix truncate for types, [#611](https://github.com/pydantic/pydantic/pull/611) by @dmontagu
* add `alias_generator` support, [#622](https://github.com/pydantic/pydantic/pull/622) by @Bobronium
* fix unparameterized generic type schema generation, [#625](https://github.com/pydantic/pydantic/pull/625) by @dmontagu
* fix schema generation with multiple/circular references to the same model, [#621](https://github.com/pydantic/pydantic/pull/621) by @tiangolo and @wongpat
* support custom root types, [#628](https://github.com/pydantic/pydantic/pull/628) by @koxudaxi
* support `self` as a field name in `parse_obj`, [#632](https://github.com/pydantic/pydantic/pull/632) by @samuelcolvin

## v0.29 (2019-06-19)

* support dataclasses.InitVar, [#592](https://github.com/pydantic/pydantic/pull/592) by @pfrederiks
* Updated documentation to elucidate the usage of `Union` when defining multiple types under an attribute's
  annotation and showcase how the type-order can affect marshalling of provided values, [#594](https://github.com/pydantic/pydantic/pull/594) by @somada141
* add `conlist` type, [#583](https://github.com/pydantic/pydantic/pull/583) by @hmvp
* add support for generics, [#595](https://github.com/pydantic/pydantic/pull/595) by @dmontagu

## v0.28 (2019-06-06)

* fix support for JSON Schema generation when using models with circular references in Python 3.7, [#572](https://github.com/pydantic/pydantic/pull/572) by @tiangolo
* support `__post_init_post_parse__` on dataclasses, [#567](https://github.com/pydantic/pydantic/pull/567) by @sevaho
* allow dumping dataclasses to JSON, [#575](https://github.com/pydantic/pydantic/pull/575) by @samuelcolvin and @DanielOberg
* ORM mode, [#562](https://github.com/pydantic/pydantic/pull/562) by @samuelcolvin
* fix `pydantic.compiled` on ipython, [#573](https://github.com/pydantic/pydantic/pull/573) by @dmontagu and @samuelcolvin
* add `StrictBool` type, [#579](https://github.com/pydantic/pydantic/pull/579) by @cazgp

## v0.27 (2019-05-30)

* **breaking change**  `_pydantic_post_init` to execute dataclass' original `__post_init__` before
  validation, [#560](https://github.com/pydantic/pydantic/pull/560) by @HeavenVolkoff
* fix handling of generic types without specified parameters, [#550](https://github.com/pydantic/pydantic/pull/550) by @dmontagu
* **breaking change** (maybe): this is the first release compiled with **cython**, see the docs and please
  submit an issue if you run into problems

## v0.27.0a1 (2019-05-26)

* fix JSON Schema for `list`, `tuple`, and `set`, [#540](https://github.com/pydantic/pydantic/pull/540) by @tiangolo
* compiling with cython, `manylinux` binaries, some other performance improvements, [#548](https://github.com/pydantic/pydantic/pull/548) by @samuelcolvin

## v0.26 (2019-05-22)

* fix to schema generation for `IPvAnyAddress`, `IPvAnyInterface`, `IPvAnyNetwork` [#498](https://github.com/pydantic/pydantic/pull/498) by @pilosus
* fix variable length tuples support, [#495](https://github.com/pydantic/pydantic/pull/495) by @pilosus
* fix return type hint for `create_model`, [#526](https://github.com/pydantic/pydantic/pull/526) by @dmontagu
* **Breaking Change:** fix `.dict(skip_keys=True)` skipping values set via alias (this involves changing
  `validate_model()` to always returns `Tuple[Dict[str, Any], Set[str], Optional[ValidationError]]`), [#517](https://github.com/pydantic/pydantic/pull/517) by @sommd
* fix to schema generation for `IPv4Address`, `IPv6Address`, `IPv4Interface`,
  `IPv6Interface`, `IPv4Network`, `IPv6Network` [#532](https://github.com/pydantic/pydantic/pull/532) by @euri10
* add `Color` type, [#504](https://github.com/pydantic/pydantic/pull/504) by @pilosus and @samuelcolvin

## v0.25 (2019-05-05)

* Improve documentation on self-referencing models and annotations, [#487](https://github.com/pydantic/pydantic/pull/487) by @theenglishway
* fix `.dict()` with extra keys, [#490](https://github.com/pydantic/pydantic/pull/490) by @JaewonKim
* support `const` keyword in `Schema`, [#434](https://github.com/pydantic/pydantic/pull/434) by @Sean1708

## v0.24 (2019-04-23)

* fix handling `ForwardRef` in sub-types, like `Union`, [#464](https://github.com/pydantic/pydantic/pull/464) by @tiangolo
* fix secret serialization, [#465](https://github.com/pydantic/pydantic/pull/465) by @atheuz
* Support custom validators for dataclasses, [#454](https://github.com/pydantic/pydantic/pull/454) by @primal100
* fix `parse_obj` to cope with dict-like objects, [#472](https://github.com/pydantic/pydantic/pull/472) by @samuelcolvin
* fix to schema generation in nested dataclass-based models, [#474](https://github.com/pydantic/pydantic/pull/474) by @NoAnyLove
* fix `json` for `Path`, `FilePath`, and `DirectoryPath` objects, [#473](https://github.com/pydantic/pydantic/pull/473) by @mikegoodspeed

## v0.23 (2019-04-04)

* improve documentation for contributing section, [#441](https://github.com/pydantic/pydantic/pull/441) by @pilosus
* improve README.rst to include essential information about the package, [#446](https://github.com/pydantic/pydantic/pull/446) by @pilosus
* `IntEnum` support, [#444](https://github.com/pydantic/pydantic/pull/444) by @potykion
* fix PyObject callable value, [#409](https://github.com/pydantic/pydantic/pull/409) by @pilosus
* fix `black` deprecation warnings after update, [#451](https://github.com/pydantic/pydantic/pull/451) by @pilosus
* fix `ForwardRef` collection bug, [#450](https://github.com/pydantic/pydantic/pull/450) by @tigerwings
* Support specialized `ClassVars`, [#455](https://github.com/pydantic/pydantic/pull/455) by @tyrylu
* fix JSON serialization for `ipaddress` types, [#333](https://github.com/pydantic/pydantic/pull/333) by @pilosus
* add `SecretStr` and `SecretBytes` types, [#452](https://github.com/pydantic/pydantic/pull/452) by @atheuz

## v0.22 (2019-03-29)

* add `IPv{4,6,Any}Network` and `IPv{4,6,Any}Interface` types from `ipaddress` stdlib, [#333](https://github.com/pydantic/pydantic/pull/333) by @pilosus
* add docs for `datetime` types, [#386](https://github.com/pydantic/pydantic/pull/386) by @pilosus
* fix to schema generation in dataclass-based models, [#408](https://github.com/pydantic/pydantic/pull/408) by @pilosus
* fix path in nested models, [#437](https://github.com/pydantic/pydantic/pull/437) by @kataev
* add `Sequence` support, [#304](https://github.com/pydantic/pydantic/pull/304) by @pilosus

## v0.21.0 (2019-03-15)

* fix typo in `NoneIsNotAllowedError` message, [#414](https://github.com/pydantic/pydantic/pull/414) by @YaraslauZhylko
* add `IPvAnyAddress`, `IPv4Address` and `IPv6Address` types, [#333](https://github.com/pydantic/pydantic/pull/333) by @pilosus

## v0.20.1 (2019-02-26)

* fix type hints of `parse_obj` and similar methods, [#405](https://github.com/pydantic/pydantic/pull/405) by @erosennin
* fix submodel validation, [#403](https://github.com/pydantic/pydantic/pull/403) by @samuelcolvin
* correct type hints for `ValidationError.json`, [#406](https://github.com/pydantic/pydantic/pull/406) by @layday

## v0.20.0 (2019-02-18)

* fix tests for Python 3.8, [#396](https://github.com/pydantic/pydantic/pull/396) by @samuelcolvin
* Adds fields to the `dir` method for autocompletion in interactive sessions, [#398](https://github.com/pydantic/pydantic/pull/398) by @dgasmith
* support `ForwardRef` (and therefore `from __future__ import annotations`) with dataclasses, [#397](https://github.com/pydantic/pydantic/pull/397) by @samuelcolvin

## v0.20.0a1 (2019-02-13)

* **breaking change** (maybe): more sophisticated argument parsing for validators, any subset of
  `values`, `config` and `field` is now permitted, eg. `(cls, value, field)`,
  however the variadic key word argument ("`**kwargs`") **must** be called `kwargs`, [#388](https://github.com/pydantic/pydantic/pull/388) by @samuelcolvin
* **breaking change**: Adds `skip_defaults` argument to `BaseModel.dict()` to allow skipping of fields that
  were not explicitly set, signature of `Model.construct()` changed, [#389](https://github.com/pydantic/pydantic/pull/389) by @dgasmith
* add `py.typed` marker file for PEP-561 support, [#391](https://github.com/pydantic/pydantic/pull/391) by @je-l
* Fix `extra` behaviour for multiple inheritance/mix-ins, [#394](https://github.com/pydantic/pydantic/pull/394) by @YaraslauZhylko

## v0.19.0 (2019-02-04)

* Support `Callable` type hint, fix [#279](https://github.com/pydantic/pydantic/pull/279) by @proofit404
* Fix schema for fields with `validator` decorator, fix [#375](https://github.com/pydantic/pydantic/pull/375) by @tiangolo
* Add `multiple_of` constraint to `ConstrainedDecimal`, `ConstrainedFloat`, `ConstrainedInt`
  and their related types `condecimal`, `confloat`, and `conint` [#371](https://github.com/pydantic/pydantic/pull/371), thanks @StephenBrown2
* Deprecated `ignore_extra` and `allow_extra` Config fields in favor of `extra`, [#352](https://github.com/pydantic/pydantic/pull/352) by @liiight
* Add type annotations to all functions, test fully with mypy, [#373](https://github.com/pydantic/pydantic/pull/373) by @samuelcolvin
* fix for 'missing' error with `validate_all` or `validate_always`, [#381](https://github.com/pydantic/pydantic/pull/381) by @samuelcolvin
* Change the second/millisecond watershed for date/datetime parsing to `2e10`, [#385](https://github.com/pydantic/pydantic/pull/385) by @samuelcolvin

## v0.18.2 (2019-01-22)

* Fix to schema generation with `Optional` fields, fix [#361](https://github.com/pydantic/pydantic/pull/361) by @samuelcolvin

## v0.18.1 (2019-01-17)

* add `ConstrainedBytes` and `conbytes` types, [#315](https://github.com/pydantic/pydantic/pull/315) @Gr1N
* adding `MANIFEST.in` to include license in package `.tar.gz`, [#358](https://github.com/pydantic/pydantic/pull/358) by @samuelcolvin

## v0.18.0 (2019-01-13)

* **breaking change**: don't call validators on keys of dictionaries, [#254](https://github.com/pydantic/pydantic/pull/254) by @samuelcolvin
* Fix validators with `always=True` when the default is `None` or the type is optional, also prevent
  `whole` validators being called for sub-fields, fix [#132](https://github.com/pydantic/pydantic/pull/132) by @samuelcolvin
* improve documentation for settings priority and allow it to be easily changed, [#343](https://github.com/pydantic/pydantic/pull/343) by @samuelcolvin
* fix `ignore_extra=False` and `allow_population_by_alias=True`, fix [#257](https://github.com/pydantic/pydantic/pull/257) by @samuelcolvin
* **breaking change**: Set `BaseConfig` attributes `min_anystr_length` and `max_anystr_length` to
  `None` by default, fix [#349](https://github.com/pydantic/pydantic/pull/349) in [#350](https://github.com/pydantic/pydantic/pull/350) by @tiangolo
* add support for postponed annotations, [#348](https://github.com/pydantic/pydantic/pull/348) by @samuelcolvin

## v0.17.0 (2018-12-27)

* fix schema for `timedelta` as number, [#325](https://github.com/pydantic/pydantic/pull/325) by @tiangolo
* prevent validators being called repeatedly after inheritance, [#327](https://github.com/pydantic/pydantic/pull/327) by @samuelcolvin
* prevent duplicate validator check in ipython, fix [#312](https://github.com/pydantic/pydantic/pull/312) by @samuelcolvin
* add "Using Pydantic" section to docs, [#323](https://github.com/pydantic/pydantic/pull/323) by @tiangolo & [#326](https://github.com/pydantic/pydantic/pull/326) by @samuelcolvin
* fix schema generation for fields annotated as `: dict`, `: list`,
  `: tuple` and `: set`, [#330](https://github.com/pydantic/pydantic/pull/330) & [#335](https://github.com/pydantic/pydantic/pull/335) by @nkonin
* add support for constrained strings as dict keys in schema, [#332](https://github.com/pydantic/pydantic/pull/332) by @tiangolo
* support for passing Config class in dataclasses decorator, [#276](https://github.com/pydantic/pydantic/pull/276) by @jarekkar
  (**breaking change**: this supersedes the `validate_assignment` argument with `config`)
* support for nested dataclasses, [#334](https://github.com/pydantic/pydantic/pull/334) by @samuelcolvin
* better errors when getting an `ImportError` with `PyObject`, [#309](https://github.com/pydantic/pydantic/pull/309) by @samuelcolvin
* rename `get_validators` to `__get_validators__`, deprecation warning on use of old name, [#338](https://github.com/pydantic/pydantic/pull/338) by @samuelcolvin
* support `ClassVar` by excluding such attributes from fields, [#184](https://github.com/pydantic/pydantic/pull/184) by @samuelcolvin

## v0.16.1 (2018-12-10)

* fix `create_model` to correctly use the passed `__config__`, [#320](https://github.com/pydantic/pydantic/pull/320) by @hugoduncan

## v0.16.0 (2018-12-03)

* **breaking change**: refactor schema generation to be compatible with JSON Schema and OpenAPI specs, [#308](https://github.com/pydantic/pydantic/pull/308) by @tiangolo
* add `schema` to `schema` module to generate top-level schemas from base models, [#308](https://github.com/pydantic/pydantic/pull/308) by @tiangolo
* add additional fields to `Schema` class to declare validation for `str` and numeric values, [#311](https://github.com/pydantic/pydantic/pull/311) by @tiangolo
* rename `_schema` to `schema` on fields, [#318](https://github.com/pydantic/pydantic/pull/318) by @samuelcolvin
* add `case_insensitive` option to `BaseSettings` `Config`, [#277](https://github.com/pydantic/pydantic/pull/277) by @jasonkuhrt

## v0.15.0 (2018-11-18)

* move codebase to use black, [#287](https://github.com/pydantic/pydantic/pull/287) by @samuelcolvin
* fix alias use in settings, [#286](https://github.com/pydantic/pydantic/pull/286) by @jasonkuhrt and @samuelcolvin
* fix datetime parsing in `parse_date`, [#298](https://github.com/pydantic/pydantic/pull/298) by @samuelcolvin
* allow dataclass inheritance, fix [#293](https://github.com/pydantic/pydantic/pull/293) by @samuelcolvin
* fix `PyObject = None`, fix [#305](https://github.com/pydantic/pydantic/pull/305) by @samuelcolvin
* allow `Pattern` type, fix [#303](https://github.com/pydantic/pydantic/pull/303) by @samuelcolvin

## v0.14.0 (2018-10-02)

* dataclasses decorator, [#269](https://github.com/pydantic/pydantic/pull/269) by @Gaunt and @samuelcolvin

## v0.13.1 (2018-09-21)

* fix issue where int_validator doesn't cast a `bool` to an `int` [#264](https://github.com/pydantic/pydantic/pull/264) by @nphyatt
* add deep copy support for `BaseModel.copy()` [#249](https://github.com/pydantic/pydantic/pull/249), @gangefors

## v0.13.0 (2018-08-25)

* raise an exception if a field's name shadows an existing `BaseModel` attribute [#242](https://github.com/pydantic/pydantic/pull/242)
* add `UrlStr` and `urlstr` types [#236](https://github.com/pydantic/pydantic/pull/236)
* timedelta json encoding ISO8601 and total seconds, custom json encoders [#247](https://github.com/pydantic/pydantic/pull/247), by @cfkanesan and @samuelcolvin
* allow `timedelta` objects as values for properties of type `timedelta` (matches `datetime` etc. behavior) [#247](https://github.com/pydantic/pydantic/pull/247)

## v0.12.1 (2018-07-31)

* fix schema generation for fields defined using `typing.Any` [#237](https://github.com/pydantic/pydantic/pull/237)

## v0.12.0 (2018-07-31)

* add `by_alias` argument in `.dict()` and `.json()` model methods [#205](https://github.com/pydantic/pydantic/pull/205)
* add Json type support [#214](https://github.com/pydantic/pydantic/pull/214)
* support tuples [#227](https://github.com/pydantic/pydantic/pull/227)
* major improvements and changes to schema [#213](https://github.com/pydantic/pydantic/pull/213)

## v0.11.2 (2018-07-05)

* add `NewType` support [#115](https://github.com/pydantic/pydantic/pull/115)
* fix `list`, `set` & `tuple` validation [#225](https://github.com/pydantic/pydantic/pull/225)
* separate out `validate_model` method, allow errors to be returned along with valid values [#221](https://github.com/pydantic/pydantic/pull/221)

## v0.11.1 (2018-07-02)

* support Python 3.7 [#216](https://github.com/pydantic/pydantic/pull/216), thanks @layday
* Allow arbitrary types in model [#209](https://github.com/pydantic/pydantic/pull/209), thanks @oldPadavan

## v0.11.0 (2018-06-28)

* make `list`, `tuple` and `set` types stricter [#86](https://github.com/pydantic/pydantic/pull/86)
* **breaking change**: remove msgpack parsing [#201](https://github.com/pydantic/pydantic/pull/201)
* add `FilePath` and `DirectoryPath` types [#10](https://github.com/pydantic/pydantic/pull/10)
* model schema generation [#190](https://github.com/pydantic/pydantic/pull/190)
* JSON serialization of models and schemas [#133](https://github.com/pydantic/pydantic/pull/133)

## v0.10.0 (2018-06-11)

* add `Config.allow_population_by_alias` [#160](https://github.com/pydantic/pydantic/pull/160), thanks @bendemaree
* **breaking change**: new errors format [#179](https://github.com/pydantic/pydantic/pull/179), thanks @Gr1N
* **breaking change**: removed `Config.min_number_size` and `Config.max_number_size` [#183](https://github.com/pydantic/pydantic/pull/183), thanks @Gr1N
* **breaking change**: correct behaviour of `lt` and `gt` arguments to `conint` etc. [#188](https://github.com/pydantic/pydantic/pull/188)
  for the old behaviour use `le` and `ge` [#194](https://github.com/pydantic/pydantic/pull/194), thanks @jaheba
* added error context and ability to redefine error message templates using `Config.error_msg_templates` [#183](https://github.com/pydantic/pydantic/pull/183),
  thanks @Gr1N
* fix typo in validator exception [#150](https://github.com/pydantic/pydantic/pull/150)
* copy defaults to model values, so different models don't share objects [#154](https://github.com/pydantic/pydantic/pull/154)

## v0.9.1 (2018-05-10)

* allow custom `get_field_config` on config classes [#159](https://github.com/pydantic/pydantic/pull/159)
* add `UUID1`, `UUID3`, `UUID4` and `UUID5` types [#167](https://github.com/pydantic/pydantic/pull/167), thanks @Gr1N
* modify some inconsistent docstrings and annotations [#173](https://github.com/pydantic/pydantic/pull/173), thanks @YannLuo
* fix type annotations for exotic types [#171](https://github.com/pydantic/pydantic/pull/171), thanks @Gr1N
* Reuse type validators in exotic types [#171](https://github.com/pydantic/pydantic/pull/171)
* scheduled monthly requirements updates [#168](https://github.com/pydantic/pydantic/pull/168)
* add `Decimal`, `ConstrainedDecimal` and `condecimal` types [#170](https://github.com/pydantic/pydantic/pull/170), thanks @Gr1N

## v0.9.0 (2018-04-28)

* tweak email-validator import error message [#145](https://github.com/pydantic/pydantic/pull/145)
* fix parse error of `parse_date()` and `parse_datetime()` when input is 0 [#144](https://github.com/pydantic/pydantic/pull/144), thanks @YannLuo
* add `Config.anystr_strip_whitespace` and `strip_whitespace` kwarg to `constr`,
  by default values is `False` [#163](https://github.com/pydantic/pydantic/pull/163), thanks @Gr1N
* add `ConstrainedFloat`, `confloat`, `PositiveFloat` and `NegativeFloat` types [#166](https://github.com/pydantic/pydantic/pull/166), thanks @Gr1N

## v0.8.0 (2018-03-25)

* fix type annotation for `inherit_config` [#139](https://github.com/pydantic/pydantic/pull/139)
* **breaking change**: check for invalid field names in validators [#140](https://github.com/pydantic/pydantic/pull/140)
* validate attributes of parent models [#141](https://github.com/pydantic/pydantic/pull/141)
* **breaking change**: email validation now uses
  [email-validator](https://github.com/JoshData/python-email-validator) [#142](https://github.com/pydantic/pydantic/pull/142)

## v0.7.1 (2018-02-07)

* fix bug with `create_model` modifying the base class

## v0.7.0 (2018-02-06)

* added compatibility with abstract base classes (ABCs) [#123](https://github.com/pydantic/pydantic/pull/123)
* add `create_model` method [#113](https://github.com/pydantic/pydantic/pull/113) [#125](https://github.com/pydantic/pydantic/pull/125)
* **breaking change**: rename `.config` to `.__config__` on a model
* **breaking change**: remove deprecated `.values()` on a model, use `.dict()` instead
* remove use of `OrderedDict` and use simple dict [#126](https://github.com/pydantic/pydantic/pull/126)
* add `Config.use_enum_values` [#127](https://github.com/pydantic/pydantic/pull/127)
* add wildcard validators of the form `@validate('*')` [#128](https://github.com/pydantic/pydantic/pull/128)

## v0.6.4 (2018-02-01)

* allow Python date and times objects [#122](https://github.com/pydantic/pydantic/pull/122)

## v0.6.3 (2017-11-26)

* fix direct install without `README.rst` present

## v0.6.2 (2017-11-13)

* errors for invalid validator use
* safer check for complex models in `Settings`

## v0.6.1 (2017-11-08)

* prevent duplicate validators, [#101](https://github.com/pydantic/pydantic/pull/101)
* add `always` kwarg to validators, [#102](https://github.com/pydantic/pydantic/pull/102)

## v0.6.0 (2017-11-07)

* assignment validation [#94](https://github.com/pydantic/pydantic/pull/94), thanks petroswork!
* JSON in environment variables for complex types, [#96](https://github.com/pydantic/pydantic/pull/96)
* add `validator` decorators for complex validation, [#97](https://github.com/pydantic/pydantic/pull/97)
* depreciate `values(...)` and replace with `.dict(...)`, [#99](https://github.com/pydantic/pydantic/pull/99)

## v0.5.0 (2017-10-23)

* add `UUID` validation [#89](https://github.com/pydantic/pydantic/pull/89)
* remove `index` and `track` from error object (json) if they're null [#90](https://github.com/pydantic/pydantic/pull/90)
* improve the error text when a list is provided rather than a dict [#90](https://github.com/pydantic/pydantic/pull/90)
* add benchmarks table to docs [#91](https://github.com/pydantic/pydantic/pull/91)

## v0.4.0 (2017-07-08)

* show length in string validation error
* fix aliases in config during inheritance [#55](https://github.com/pydantic/pydantic/pull/55)
* simplify error display
* use unicode ellipsis in `truncate`
* add `parse_obj`, `parse_raw` and `parse_file` helper functions [#58](https://github.com/pydantic/pydantic/pull/58)
* switch annotation only fields to come first in fields list not last

## v0.3.0 (2017-06-21)

* immutable models via `config.allow_mutation = False`, associated cleanup and performance improvement [#44](https://github.com/pydantic/pydantic/pull/44)
* immutable helper methods `construct()` and `copy()` [#53](https://github.com/pydantic/pydantic/pull/53)
* allow pickling of models [#53](https://github.com/pydantic/pydantic/pull/53)
* `setattr` is removed as `__setattr__` is now intelligent [#44](https://github.com/pydantic/pydantic/pull/44)
* `raise_exception` removed, Models now always raise exceptions [#44](https://github.com/pydantic/pydantic/pull/44)
* instance method validators removed
* django-restful-framework benchmarks added [#47](https://github.com/pydantic/pydantic/pull/47)
* fix inheritance bug [#49](https://github.com/pydantic/pydantic/pull/49)
* make str type stricter so list, dict etc are not coerced to strings. [#52](https://github.com/pydantic/pydantic/pull/52)
* add `StrictStr` which only always strings as input [#52](https://github.com/pydantic/pydantic/pull/52)

## v0.2.1 (2017-06-07)

* pypi and travis together messed up the deploy of `v0.2` this should fix it

## v0.2.0 (2017-06-07)

* **breaking change**: `values()` on a model is now a method not a property,
  takes `include` and `exclude` arguments
* allow annotation only fields to support mypy
* add pretty `to_string(pretty=True)` method for models

## v0.1.0 (2017-06-03)

* add docs
* add history
