---
x-trestle-set-params:
    # This section contains the parameters that are part of this control.
  # Each parameter has properties. Only the profile-values and display-name properties are editable.
  # The other properties are informational.
  #
  # The values property for a parameter represents values inherited from the OSCAL catalog.
  # To override the catalog settings, use bullets under profile-values as shown below:
  #
  #   profile-values:
  #     - value 1
  #     - value 2
  #
  # If the "- <REPLACE_ME>" placeholder appears under profile-values, it is the same as if
  # the profile-values property were left empty.
  #
  # Some parameters may show an aggregates property which lists other parameters. This means
  # the parameter value is made up of the values from the other parameters. For parameters
  # that aggregate, profile-values is not applicable.
  #
  # Property param-value-origin is meant for putting the origin from where that parameter comes from.
  # In order to be changed in the current profile, profile-param-value-origin property will be displayed with
  # the placeholder "<REPLACE_ME>" for you to be replaced. If a parameter already has a param-value-origin
  # coming from an inherited profile, do no change this value, instead use profile-param-value-origin as follows:
  #
  #    param-value-origin: DO NOT REPLACE - this is the original value
  #    profile-param-value-origin: <REPLACE_ME> - replace the new value required HERE
  #
  si-04_odp.01:
    alt-identifier: si-4_prm_1
    profile-values:
      - <REPLACE_ME>
    profile-param-value-origin: <REPLACE_ME>
  si-04_odp.02:
    alt-identifier: si-4_prm_2
    profile-values:
      - <REPLACE_ME>
    profile-param-value-origin: <REPLACE_ME>
  si-04_odp.03:
    alt-identifier: si-4_prm_3
    profile-values:
      - <REPLACE_ME>
    profile-param-value-origin: <REPLACE_ME>
  si-04_odp.04:
    alt-identifier: si-4_prm_4
    profile-values:
      - <REPLACE_ME>
    profile-param-value-origin: <REPLACE_ME>
  si-04_odp.05:
    alt-identifier: si-4_prm_5
    profile-values:
      - <REPLACE_ME>
    profile-param-value-origin: <REPLACE_ME>
  si-04_odp.06:
    alt-identifier: si-4_prm_6
    profile-values:
      - <REPLACE_ME>
    profile-param-value-origin: <REPLACE_ME>
x-trestle-global:
  profile:
    title: NIST Special Publication 800-53 Revision 5 HIGH IMPACT BASELINE
  sort-id: si-04
---

# si-4 - \[System and Information Integrity\] System Monitoring

## Control Statement

- \[a.\] Monitor the system to detect:

  - \[1.\] Attacks and indicators of potential attacks in accordance with the following monitoring objectives: {{ insert: param, si-04_odp.01 }} ; and
  - \[2.\] Unauthorized local, network, and remote connections;

- \[b.\] Identify unauthorized use of the system through the following techniques and methods: {{ insert: param, si-04_odp.02 }};

- \[c.\] Invoke internal monitoring capabilities or deploy monitoring devices:

  - \[1.\] Strategically within the system to collect organization-determined essential information; and
  - \[2.\] At ad hoc locations within the system to track specific types of transactions of interest to the organization;

- \[d.\] Analyze detected events and anomalies;

- \[e.\] Adjust the level of system monitoring activity when there is a change in risk to organizational operations and assets, individuals, other organizations, or the Nation;

- \[f.\] Obtain legal opinion regarding system monitoring activities; and

- \[g.\] Provide {{ insert: param, si-04_odp.03 }} to {{ insert: param, si-04_odp.04 }} {{ insert: param, si-04_odp.05 }}.

## Control Assessment Objective

- \[SI-04a.\]

  - \[SI-04a.01\] the system is monitored to detect attacks and indicators of potential attacks in accordance with {{ insert: param, si-04_odp.01 }};
  - \[SI-04a.02\]

    - \[SI-04a.02[01]\] the system is monitored to detect unauthorized local connections;
    - \[SI-04a.02[02]\] the system is monitored to detect unauthorized network connections;
    - \[SI-04a.02[03]\] the system is monitored to detect unauthorized remote connections;

- \[SI-04b.\] unauthorized use of the system is identified through {{ insert: param, si-04_odp.02 }};

- \[SI-04c.\]

  - \[SI-04c.01\] internal monitoring capabilities are invoked or monitoring devices are deployed strategically within the system to collect organization-determined essential information;
  - \[SI-04c.02\] internal monitoring capabilities are invoked or monitoring devices are deployed at ad hoc locations within the system to track specific types of transactions of interest to the organization;

- \[SI-04d.\]

  - \[SI-04d.[01]\] detected events are analyzed;
  - \[SI-04d.[02]\] detected anomalies are analyzed;

- \[SI-04e.\] the level of system monitoring activity is adjusted when there is a change in risk to organizational operations and assets, individuals, other organizations, or the Nation;

- \[SI-04f.\] a legal opinion regarding system monitoring activities is obtained;

- \[SI-04g.\] {{ insert: param, si-04_odp.03 }} is provided to {{ insert: param, si-04_odp.04 }} {{ insert: param, si-04_odp.05 }}.

## Control guidance

System monitoring includes external and internal monitoring. External monitoring includes the observation of events occurring at external interfaces to the system. Internal monitoring includes the observation of events occurring within the system. Organizations monitor systems by observing audit activities in real time or by observing other system aspects such as access patterns, characteristics of access, and other actions. The monitoring objectives guide and inform the determination of the events. System monitoring capabilities are achieved through a variety of tools and techniques, including intrusion detection and prevention systems, malicious code protection software, scanning tools, audit record monitoring software, and network monitoring software.

Depending on the security architecture, the distribution and configuration of monitoring devices may impact throughput at key internal and external boundaries as well as at other locations across a network due to the introduction of network throughput latency. If throughput management is needed, such devices are strategically located and deployed as part of an established organization-wide security architecture. Strategic locations for monitoring devices include selected perimeter locations and near key servers and server farms that support critical applications. Monitoring devices are typically employed at the managed interfaces associated with controls [SC-7](#sc-7) and [AC-17](#ac-17) . The information collected is a function of the organizational monitoring objectives and the capability of systems to support such objectives. Specific types of transactions of interest include Hypertext Transfer Protocol (HTTP) traffic that bypasses HTTP proxies. System monitoring is an integral part of organizational continuous monitoring and incident response programs, and output from system monitoring serves as input to those programs. System monitoring requirements, including the need for specific types of system monitoring, may be referenced in other controls (e.g., [AC-2g](#ac-2_smt.g), [AC-2(7)](#ac-2.7), [AC-2(12)(a)](#ac-2.12_smt.a), [AC-17(1)](#ac-17.1), [AU-13](#au-13), [AU-13(1)](#au-13.1), [AU-13(2)](#au-13.2), [CM-3f](#cm-3_smt.f), [CM-6d](#cm-6_smt.d), [MA-3a](#ma-3_smt.a), [MA-4a](#ma-4_smt.a), [SC-5(3)(b)](#sc-5.3_smt.b), [SC-7a](#sc-7_smt.a), [SC-7(24)(b)](#sc-7.24_smt.b), [SC-18b](#sc-18_smt.b), [SC-43b](#sc-43_smt.b) ). Adjustments to levels of system monitoring are based on law enforcement information, intelligence information, or other sources of information. The legality of system monitoring activities is based on applicable laws, executive orders, directives, regulations, policies, standards, and guidelines.

# Editable Content

<!-- Make additions and edits below -->
<!-- The above represents the contents of the control as received by the profile, prior to additions. -->
<!-- If the profile makes additions to the control, they will appear below. -->
<!-- The above markdown may not be edited but you may edit the content below, and/or introduce new additions to be made by the profile. -->
<!-- If there is a yaml header at the top, parameter values may be edited. Use --set-parameters to incorporate the changes during assembly. -->
<!-- The content here will then replace what is in the profile for this control, after running profile-assemble. -->
<!-- The current profile has no added parts for this control, but you may add new ones here. -->
<!-- Each addition must have a heading either of the form ## Control my_addition_name -->
<!-- or ## Part a. (where the a. refers to one of the control statement labels.) -->
<!-- "## Control" parts are new parts added after the statement part. -->
<!-- "## Part" parts are new parts added into the top-level statement part with that label. -->
<!-- Subparts may be added with nested hash levels of the form ### My Subpart Name -->
<!-- underneath the parent ## Control or ## Part being added -->
<!-- See https://oscal-compass.github.io/compliance-trestle/tutorials/ssp_profile_catalog_authoring/ssp_profile_catalog_authoring for guidance. -->
