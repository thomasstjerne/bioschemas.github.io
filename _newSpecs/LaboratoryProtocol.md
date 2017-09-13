---
description: 'An experimental protocol is a sequence of tasks and operations executed
  to perform experimental research in biological and biomedical areas.

  Experimental protocols are fundamental information structures that support the description
  of the processes by means of which results are generated in experimental research
  [1]. Experimental protocols describe how the data were produced, the steps undertaken
  and conditions under which these steps were carried out.

  [1]  Giraldo, O., Garcia, A., Corcho, O.: SMART Protocols: SeMAntic RepresenTation
  for Experimental Protocols, Riva del Garda, Trentino, Italy (2014). 4th Workshop
  on Linked Science 2014- Making Sense Out of Data (LISC2014)

  '
edit_url: https://github.com/BioSchemas/bioschemas.github.io/edit/master/_newSpecs/LaboratoryProtocol.md
extended_props:
  CreativeWork:
  - bsc_dec: ''
    cardinality: MANY
    controlled_vocab:
      ontologies: []
      terms: []
    expected_type:
    - CreativeWork
    - URL
    marginality: Recommended
    name: citation
    sdo_desc: A citation or reference to another creative work, such as another publication,
      web page, scholarly article, etc.
  - bsc_dec: ''
    cardinality: ONE
    controlled_vocab:
      ontologies: []
      terms: []
    expected_type:
    - CreativeWork
    - URL
    marginality: Minimum
    name: license
    sdo_desc: A license document that applies to this content, typically indicated
      by URL.
  - bsc_dec: ''
    cardinality: MANY
    controlled_vocab:
      ontologies: []
      terms: []
    expected_type:
    - CreativeWork
    - URL
    marginality: Recommended
    name: isBasedOn
    sdo_desc: A resource that was used in the creation of this resource. This term
      can be repeated for multiple sources. For example, http://example.com/great-multiplication-intro.html.
  - bsc_dec: ''
    cardinality: MANY
    controlled_vocab:
      ontologies: []
      terms: []
    expected_type:
    - CreativeWork
    marginality: Recommended
    name: isPartOf
    sdo_desc: Indicates a CreativeWork that this CreativeWork is (in some sense) part
      of.
  - bsc_dec: ''
    cardinality: MANY
    controlled_vocab:
      ontologies: []
      terms: []
    expected_type:
    - Text
    marginality: Recommended
    name: keywords
    sdo_desc: Keywords or tags used to describe this content. Multiple entries in
      a keywords list are typically delimited by commas.
  Thing:
  - bsc_dec: ''
    cardinality: ONE
    controlled_vocab:
      ontologies:
      - name: SmartProtocols (http
        url: //bioportal.bioontology.org/ontologies/SP)
      terms: []
    expected_type:
    - URL
    marginality: Optional
    name: additionalType
    sdo_desc: An additional type for the item, typically used for adding more specific
      types from external vocabularies in microdata syntax. This is a relationship
      between something and a class that the thing is in. In RDFa syntax, it is better
      to use the native RDFa syntax - the 'typeof' attribute - for multiple types.
      Schema.org tools may have only weaker understanding of extra types, in particular
      those defined externally.
  - bsc_dec: ''
    cardinality: ONE
    controlled_vocab:
      ontologies: []
      terms: []
    expected_type:
    - PropertyValue, Text, URL
    marginality: Minimum
    name: identifier
    sdo_desc: The identifier property represents any kind of identifier for any kind
      of <a class="localLink" href="http://schema.org/Thing">Thing</a>, such as ISBNs,
      GTIN codes, UUIDs etc. Schema.org provides dedicated properties for representing
      many of these, either as textual strings or as URL (URI) links. See <a href="/docs/datamodel.html#identifierBg">background
      notes</a> for more details.
g_mapping_file: LabProtocol Mapping
gh_folder: https://github.com/BioSchemas/LaboratoryProtocol
gh_tasks: https://github.com/BioSchemas/bioschemas/labels/type%3A%20LaboratoryProtocol
hierarchy:
- CreativeWork
- Thing
layout: new_spec_detail
name: LaboratoryProtocol
new_props:
- bsc_dec: ''
  cardinality: MANY
  controlled_vocab:
    ontologies:
    - name: SmartProtocols (http
      url: //bioportal.bioontology.org/ontologies/SP)
    terms: []
  expected_type:
  - CreativeWork
  marginality: Recommended
  name: structuralElement
  sdo_desc: A structural element refers to qualified text in a CreativeWork. It should
    be used when plain text is not enough, for instance, to distinguish abstract,
    sections or paragraphs. Qualification is achieved by using the additionaType property
    which should point to an ontological term describing the element referred to by
    this property. The text itself can be added using the property text.  Bioschemas
    usage.  A particular case in Bioschemas is LabProtocol where structural elements
    are used to described advantages (situations the Protocol has been successfully
    employed), limitations (situations the Protocol would be unreliable or otherwise
    unsuccessful), applications (Applications of the protocol list the full diversity
    of the applications of the method and support if is possible to extend the range
    of applications of the protocol. e.g. northern blot assays, sequencing, etc.),
    and outcomes (outcome or expected result by a protocol execution).  For LabProtocol,
    in the applicationType, please use http://purl.org/net/SMARTprotocol#AdvantageOfTheProtocol
    for advantages, http://purl.org/net/SMARTprotocol#LimitationOfTheProtocol for
    limitations, http://purl.org/net/SMARTprotocol#ApplicationOfTheProtocol for applicability,
    and http://purl.org/net/SMARTprotocol#OutcomeOfTheProtocol for outcomes.
- bsc_dec: ''
  cardinality: MANY
  controlled_vocab:
    ontologies: []
    terms: []
  expected_type:
  - PhysicalEntity, Text
  - URL
  marginality: Minimum
  name: reagent
  sdo_desc: Reagent used in the protocol. It can be a record in a Dataset describing
    the reagent or a PhysicalEntity corresponding to the reagent or a URL pointing
    to the type of reagent used. ChEBI and PubChem entities can be used whenever available.
    Commercial names are also acceptable (URL if possible)
- bsc_dec: ''
  cardinality: MANY
  controlled_vocab:
    ontologies: []
    terms: []
  expected_type:
  - Text
  marginality: Minimum
  name: purpose
  sdo_desc: A goal towards an action is taken. Can be concrete or abstract.
- bsc_dec: ''
  cardinality: MANY
  controlled_vocab:
    ontologies: []
    terms: []
  expected_type:
  - Thing, Text
  - URL
  marginality: Minimum
  name: instrument
  sdo_desc: The object that helped the agent perform the action. e.g. John wrote a
    book with a pen.  For LabProtocols it would be a laboratory equipment use by a
    person to follow one or more steps described in this LabProtocol.
- bsc_dec: ''
  cardinality: MANY
  controlled_vocab:
    ontologies: []
    terms: []
  expected_type:
  - PhysicalEntity, Text
  - URL
  marginality: Minimum
  name: sample
  sdo_desc: Sample used in the protocol. It could be a record in a Dataset describing
    the sample or a physical object corresponding to the sample or a URL pointing
    to the type of sample used.
- bsc_dec: ''
  cardinality: MANY
  controlled_vocab:
    ontologies: []
    terms: []
  expected_type:
  - SoftwareApplication
  marginality: Recommended
  name: software
  sdo_desc: An application that can complete the request.
- bsc_dec: ''
  cardinality: ONE
  controlled_vocab:
    ontologies: []
    terms: []
  expected_type:
  - Duration
  marginality: Recommended
  name: duration
  sdo_desc: The time it takes to actually carry on the protocol, in ISO 8601 duration
    format.
parent_type: CreativeWork
spec_mapping_url: https://docs.google.com/spreadsheets/d/1julB0P6kjXK_mL2dU8EDU9zMxIMah0_dYYeGt2Spllo/edit?usp=drivesdk
spec_type: Type
status: revision
subtitle: Bioschemas specification describing LabProtocol in the life-science.
version: 0.0.1
---