# Awesome Italian PA opensource [![Awesome](https://awesome.re/badge.svg)](https://awesome.re) [![Contributions Welcome](https://img.shields.io/badge/contributions-welcome-brightgreen.svg)](CONTRIBUTING.md) [![Last Updated](https://img.shields.io/badge/last%20updated-March%202026-blue.svg)](#)

A curated list of open-source libraries, tools, and resources for integrating Italian Public Administration services into software applications.

> 🇮🇹 **Per gli sviluppatori italiani:** Questa lista raccoglie le migliori librerie open source per integrare i servizi della Pubblica Amministrazione italiana (SPID, CIE, Fattura Elettronica, PEC, ANPR, pagoPA, ecc.) nelle tue applicazioni. Contribuisci aggiungendo risorse che usi nei tuoi progetti!

---

## Contents

- [Identity \& Authentication](#-identity--authentication)
  - [SPID](#spid)
  - [CIE](#cie)
  - [CNS / TS-CNS](#cns--ts-cns)
  - [Multi-protocol (SPID + CIE + eIDAS)](#multi-protocol-spid--cie--eidas)
- [Invoicing \& Tax](#-invoicing--tax)
  - [Fattura Elettronica / SDI](#fattura-elettronica--sdi)
  - [Codice Fiscale](#codice-fiscale)
  - [Partita IVA Validation](#partita-iva-validation)
- [Digital Signatures \& P7M](#-digital-signatures--p7m)
- [Communication](#-communication)
  - [PEC](#pec)
  - [SEND (Piattaforma Notifiche)](#send-piattaforma-notifiche)
- [Registries \& Open Data](#-registries--open-data)
  - [ANPR](#anpr)
  - [ANNCSU](#anncsu)
  - [Comuni / CAP / ISTAT](#comuni--cap--istat)
  - [Catasto / SISTER](#catasto--sister)
  - [Fiscal \& Budget Data](#fiscal--budget-data)
  - [Normativa / Legal Texts](#normativa--legal-texts)
  - [Open Data Portals \& Semantic Assets](#open-data-portals--semantic-assets)
- [Healthcare](#-healthcare)
  - [FSE (Fascicolo Sanitario Elettronico)](#fse-fascicolo-sanitario-elettronico)
  - [Tessera Sanitaria](#tessera-sanitaria)
- [Design \& UI](#-design--ui)
  - [Bootstrap Italia / Design System](#bootstrap-italia--design-system)
  - [Framework Integrations](#framework-integrations)
- [Multi-service SDKs \& Platforms](#-multi-service-sdks--platforms)
  - [IO App / pagoPA](#io-app--pagopa)
  - [PDND (Piattaforma Digitale Nazionale Dati)](#pdnd-piattaforma-digitale-nazionale-dati)
  - [Developers Italia](#developers-italia)

---

## 🪪 Identity & Authentication

### SPID

[SPID](https://www.spid.gov.it/) (Sistema Pubblico di Identità Digitale) is Italy's national digital identity system. It allows citizens to access online public services with a single set of credentials. Integration typically uses SAML2 or OIDC protocols.

#### Official / Core

- [italia/spid](https://github.com/italia/spid) — Official SPID documentation and technical resources.
- [italia/spid-saml-check](https://github.com/italia/spid-saml-check) — SAML implementation compliance checker for SPID Service Providers. `JavaScript`
- [italia/spid-sp-test](https://github.com/italia/spid-sp-test) — SAML2 SPID/CIE Service Provider validation tool. `Python`
- [italia/spid-sp-access-button](https://github.com/italia/spid-sp-access-button) — Official "Login with SPID" button with IdP chooser. `HTML/CSS`
- [italia/spid-smart-button](https://github.com/italia/spid-smart-button) — JavaScript modal-based SPID login button. `JavaScript`
- [italia/spid-compliant-certificates](https://github.com/italia/spid-compliant-certificates) — Generate X.509 certificates compliant with SPID technical specs. `Shell`
- [italia/spid-compliant-certificates-python](https://github.com/italia/spid-compliant-certificates-python) — Python-native X.509 certificate generator for SPID. `Python`
- [italia/spid-regole-tecniche](https://github.com/italia/spid-regole-tecniche) — SPID technical specifications (regole tecniche). `Docs`
- [italia/spid-metadata-signer](https://github.com/italia/spid-metadata-signer) — Tool for signing SPID SAML metadata. `Shell`

#### SAML Libraries

- [italia/spid-cie-php](https://github.com/italia/spid-cie-php) — SPID/CIE SDK for PHP with SimpleSAMLphp. `PHP`
- [italia/spid-laravel](https://github.com/italia/spid-laravel) — SPID authentication package for Laravel. `PHP`
- [italia/spid-php-lib](https://github.com/italia/spid-php-lib) — Standalone PHP library for SPID authentication. `PHP`
- [italia/spid-django](https://github.com/italia/spid-django) — SPID authentication for Django. `Python`
- [italia/spid-keycloak-provider](https://github.com/italia/spid-keycloak-provider) — SPID authentication provider for Keycloak. `Java`
- [italia/spid-spring](https://github.com/italia/spid-spring) — SPID extension for Java Spring. `Java` ⚠️ *unmaintained*
- [italia/spid-aspnetcore](https://github.com/italia/spid-aspnetcore) — SPID Remote Authenticator for ASP.NET Core. `C#`
- [italia/spid-dotnet-sdk](https://github.com/italia/spid-dotnet-sdk) — SPID authentication library for .NET. `C#`
- [italia/spid-go](https://github.com/italia/spid-go) — Go package for SPID authentication. `Go`
- [italia/spid-passport](https://github.com/italia/spid-passport) — Passport.js authentication strategy for SPID. `JavaScript` ⚠️ *unmaintained*
- [dej611/spid-react-button](https://github.com/dej611/spid-react-button) — SPID SSO login button component for React. `TypeScript`
- [WPGov/wp-spid-italia](https://github.com/WPGov/wp-spid-italia) — SPID integration plugin for WordPress. `PHP`
- [italia/spid-shibboleth-proxy-docker](https://github.com/italia/spid-shibboleth-proxy-docker) — SPID authentication proxy based on Shibboleth SP (Docker). `Docker` ⚠️ *unmaintained*
- [microsoft/SPID-and-Digital-Identity-Enabler](https://github.com/microsoft/SPID-and-Digital-Identity-Enabler) — SPID proxy for ADFS/Azure AD B2C. `C#`
- [INPS-it/SPIDlibraryAndroid](https://github.com/INPS-it/SPIDlibraryAndroid) — SPID login library for Android with multiple IdP support. `Kotlin`
- [INPS-it/SPIDlibraryIOS](https://github.com/INPS-it/SPIDlibraryIOS) — SPID login library for iOS with multiple IdP support. `Swift`

#### OIDC Libraries

- [italia/spid-cie-oidc-django](https://github.com/italia/spid-cie-oidc-django) — SPID/CIE OIDC Federation SDK for Django. `Python`
- [italia/spid-cie-oidc-java](https://github.com/italia/spid-cie-oidc-java) — SPID/CIE OIDC Federation Relying Party for Java. `Java`
- [italia/spid-cie-oidc-php](https://github.com/italia/spid-cie-oidc-php) — SPID/CIE OIDC Federation Relying Party for PHP. `PHP`
- [italia/spid-cie-oidc-aspnetcore](https://github.com/italia/spid-cie-oidc-aspnetcore) — SPID/CIE OIDC Federation SDK for ASP.NET Core. `C#`

#### Test & Development

- [italia/spid-testenv2](https://github.com/italia/spid-testenv2) — Test Identity Provider for SPID development. `Python` ⚠️ *unmaintained*

### CIE

[CIE](https://www.cartaidentita.interno.gov.it/) (Carta d'Identità Elettronica) is Italy's electronic identity card. It includes an NFC chip and can be used for digital authentication via OIDC or physical reading via MRTD/NIS protocols.

- [italia/cie-middleware](https://github.com/italia/cie-middleware) — CIE desktop middleware (Windows/macOS). `C++`
- [italia/cie-middleware-linux](https://github.com/italia/cie-middleware-linux) — CIE middleware for Linux. `C++`
- [italia/cie-nis-python-sdk](https://github.com/italia/cie-nis-python-sdk) — SDK for reading the NIS code from CIE via NFC. `Python`
- [italia/cie-PN532](https://github.com/italia/cie-PN532) — Arduino library for NFC access to CIE chip. `C++`
- [italia/cie-mrtd-dotnet-sdk](https://github.com/italia/cie-mrtd-dotnet-sdk) — SDK for reading ICAO MRTD data from CIE. `.NET`
- [italia/cie-ideaapp](https://github.com/italia/cie-ideaapp) — Android app for reading CIE ICAO data. `Java`

### CNS / TS-CNS

[CNS](https://www.agid.gov.it/) (Carta Nazionale dei Servizi) and TS-CNS (Tessera Sanitaria - CNS) are smart cards used for digital authentication with public services, primarily in healthcare.

- [italia/cie-cns-apache-docker](https://github.com/italia/cie-cns-apache-docker) — Docker-based Apache template for CIE/CNS smart card authentication. `Docker`

### Multi-protocol (SPID + CIE + eIDAS)

- [italia/iam-proxy-italia](https://github.com/italia/iam-proxy-italia) — IAM Proxy supporting SPID/CIE/eIDAS with SAML2, OIDC, and OpenID4VC. `JavaScript`
- [AgID/eidas-italian-node](https://github.com/AgID/eidas-italian-node) — Italian eIDAS node for cross-border authentication under the EU eIDAS regulation. `HTML`
- [andry08/ArubaOTP-seed-extractor](https://github.com/andry08/ArubaOTP-seed-extractor) — Extract TOTP seed from ArubaOTP app (commonly used with SPID). `Python`

---

## 🧾 Invoicing & Tax

### Fattura Elettronica / SDI

[Fattura Elettronica](https://www.fatturapa.gov.it/) is Italy's mandatory electronic invoicing system. Invoices are XML documents exchanged through SDI (Sistema di Interscambio), the government's exchange hub.

- [FatturaElettronica/FatturaElettronica.NET](https://github.com/FatturaElettronica/FatturaElettronica.NET) — Full-featured e-invoice library for .NET (B2B and B2G). `C#`
- [deved-it/fattura-elettronica](https://github.com/deved-it/fattura-elettronica) — Italian electronic invoicing library. `PHP`
- [taocomp/php-e-invoice-it](https://github.com/taocomp/php-e-invoice-it) — PHP package for managing Italian e-invoice XML formats. `PHP`
- [Truelite/python-a38](https://github.com/Truelite/python-a38) — Python library for working with Fattura Elettronica. `Python`
- [fatturaelettronicaphp/FatturaElettronica](https://github.com/fatturaelettronicaphp/FatturaElettronica) — PHP library for reading, generating, and validating e-invoices. `PHP`
- [phax/ph-fatturapa](https://github.com/phax/ph-fatturapa) — Java library for reading/writing FatturaPA 1.2.x invoices. `Java`
- [Slamdunk/php-validatore-fattura-elettronica](https://github.com/Slamdunk/php-validatore-fattura-elettronica) — XML validator for Fattura Elettronica. `PHP`
- [andreafalzetti/node-fatturazione-elettronica-aruba](https://github.com/andreafalzetti/node-fatturazione-elettronica-aruba) — Node.js client for Aruba electronic invoicing API. `JavaScript`

### Codice Fiscale

The [Codice Fiscale](https://www.agenziaentrate.gov.it/) is Italy's tax identification code — a 16-character alphanumeric string assigned to every person. Libraries below handle generation, validation, and parsing.

- [lucavandro/CodiceFiscaleJS](https://github.com/lucavandro/CodiceFiscaleJS) — Compute and validate Italian tax codes. `JavaScript`
- [DavidePastore/codice-fiscale](https://github.com/DavidePastore/codice-fiscale) — Calculate and validate Codice Fiscale. `PHP`
- [fabiocaccamo/python-codicefiscale](https://github.com/fabiocaccamo/python-codicefiscale) — Encoding, decoding, and validation of Italian fiscal codes. `Python`
- [robertogallea/laravel-codicefiscale](https://github.com/robertogallea/laravel-codicefiscale) — Codice Fiscale validation for Laravel. `PHP`
- [Marketto/codice-fiscale-utils](https://github.com/Marketto/codice-fiscale-utils) — Full-featured Codice Fiscale utility library. `TypeScript`
- [topac/codice_fiscale](https://github.com/topac/codice_fiscale) — Ruby gem for calculating Italian tax codes. `Ruby`
- [matteoredz/itax-code](https://github.com/matteoredz/itax-code) — Ruby gem for Italian tax codes (generation, validation, parsing). `Ruby`
- [ema/pycodicefiscale](https://github.com/ema/pycodicefiscale) — Python library for Codice Fiscale handling. `Python`
- [kamaladafrica/codice-fiscale](https://github.com/kamaladafrica/codice-fiscale) — Java Codice Fiscale calculator. `Java`
- [squeeze69/codicefiscale](https://github.com/squeeze69/codicefiscale) — Italian Codice Fiscale validator. `Go`
- [alessandroamella/codice-fiscale-ts](https://github.com/alessandroamella/codice-fiscale-ts) — TypeScript library for Codice Fiscale calculation and validation. `TypeScript`

### Partita IVA Validation

The Partita IVA is the Italian VAT identification number — an 11-digit code assigned to businesses and professionals.

- [squeeze69/partitaiva](https://github.com/squeeze69/partitaiva) — Italian Partita IVA validator. `Go`
- [dennybiasiolli/node-cfpiva](https://github.com/dennybiasiolli/node-cfpiva) — Combined Codice Fiscale + Partita IVA validation. `JavaScript`

---

## ✍️ Digital Signatures & P7M

Italian law requires digital signatures (CAdES, PAdES, XAdES) for many official documents. CAdES signatures produce `.p7m` files — PKCS#7 envelopes wrapping the signed document. These tools handle signing, verification, and extraction of `.p7m` content.

- [eniocarboni/p7m](https://github.com/eniocarboni/p7m) — Shell script for managing CAdES digitally signed `.p7m` files. `Shell`
- [damianofalcioni/Websocket-Smart-Card-Signer](https://github.com/damianofalcioni/Websocket-Smart-Card-Signer) — Websocket-based (no applet) smart card digital signature framework. `Java`
- [FatturaElettronica/FatturaElettronica.Extensions](https://github.com/FatturaElettronica/FatturaElettronica.Extensions) — .NET extension for reading and signing e-invoices as `.p7m`. `C#`
- [Adibla/p7m-decoder](https://github.com/Adibla/p7m-decoder) — Node.js P7M decoder. `TypeScript`
- [filippotoso/p7m-extractor](https://github.com/filippotoso/p7m-extractor) — Extract the original file from a signed `.p7m` envelope. `PHP`
- [Slamdunk/php-p7m-reader](https://github.com/Slamdunk/php-p7m-reader) — PHP library for reading `.p7m` files. `PHP`
- [eutampieri/digifirma](https://github.com/eutampieri/digifirma) — Italian CIE-based P7M parser and signature checker. `Rust`

---

## 📮 Communication

### PEC

[PEC](https://www.agid.gov.it/) (Posta Elettronica Certificata) is Italy's certified email system. PEC messages have legal validity equivalent to registered mail. It's based on standard email protocols (SMTP/IMAP) with added S/MIME signatures and delivery receipts.

- [biagioT/java-pec-parser](https://github.com/biagioT/java-pec-parser) — Java library for parsing PEC messages and delivery receipts. `Java`
- [danzipie/go-pec-tool](https://github.com/danzipie/go-pec-tool) — CLI tool for PEC operations. `Go`

### SEND (Piattaforma Notifiche)

[SEND](https://notifichedigitali.pagopa.it/) (previously "Piattaforma Notifiche") is Italy's digital notification platform operated by pagoPA. It enables public administrations to send legally valid digital notifications to citizens.

- [pagopa/pn-frontend](https://github.com/pagopa/pn-frontend) — Frontend for the SEND digital notification platform. `TypeScript`
- [pagopa/pn-local-emulator](https://github.com/pagopa/pn-local-emulator) — Local emulator of the SEND HTTP API for development. `TypeScript`

---

## 🗃️ Registries & Open Data

### ANPR

[ANPR](https://www.anagrafenazionale.interno.it/) (Anagrafe Nazionale della Popolazione Residente) is Italy's centralized civil registry, replacing local municipal registries. It holds demographic data for all residents.

- [italia/anpr](https://github.com/italia/anpr) — Official ANPR documentation and issue tracker. `Docs`
- [italia/anpr-client-example](https://github.com/italia/anpr-client-example) — Example Java client for connecting to ANPR APIs. `Java`

### ANNCSU

[ANNCSU](https://www.anncsu.gov.it/) (Archivio Nazionale dei Numeri Civici e delle Strade Urbane) is Italy's national archive of street addresses and house numbers, jointly managed by ISTAT and Agenzia delle Entrate.

- [ondata/archivio_anncsu](https://github.com/ondata/archivio_anncsu) — Tools for accessing and processing ANNCSU address data. `Shell`

### Comuni / CAP / ISTAT

Open datasets of Italian municipalities, postal codes (CAP), and ISTAT statistical codes. Essential for address validation, form autocomplete, and geographic lookups.

- [matteocontrini/comuni-json](https://github.com/matteocontrini/comuni-json) — JSON database of Italian municipalities with ISTAT codes and CAP. `JSON`
- [MatteoHenryChinaski/Comuni-Italiani-2018-Sql-Json-excel](https://github.com/MatteoHenryChinaski/Comuni-Italiani-2018-Sql-Json-excel) — Italian municipalities database in SQL, JSON, and Excel formats. `SQL`
- [Samurai016/Comuni-ITA](https://github.com/Samurai016/Comuni-ITA) — REST API for Italian municipalities in JSON/XML/CSV. `TypeScript`
- [ondata/guida-api-istat](https://github.com/ondata/guida-api-istat) — Comprehensive guide to ISTAT REST APIs with examples and documentation. `Shell`

### Catasto / SISTER

[SISTER](https://sister.agenziaentrate.gov.it/) (Sistema Integrato del Territorio) is the Agenzia delle Entrate's portal for accessing Italian cadastral data (land and building registry). It provides land parcel details, property ownership records, and territorial sections.

- [zornade/visura-api](https://github.com/zornade/visura-api) — API service for automated cadastral data extraction from the SISTER portal, with SPID authentication (Sielte ID). `Python`
- [ondata/dati_catastali](https://github.com/ondata/dati_catastali) — Query Italian cadastral data by attribute (land parcels, ownership). `Shell`

### Fiscal & Budget Data

Public-finance data published by MEF and Banca d'Italia — including [SIOPE](https://www.siope.it/) (Sistema Informativo Operazioni Enti Pubblici), tracking cash flows of Italian public entities, and [OpenBDAP](https://openbdap.mef.gov.it/) (Banca Dati Amministrazioni Pubbliche), the Ragioneria Generale dello Stato portal for fiscal accounts.

- [dataciviclab/siope-comuni](https://github.com/dataciviclab/siope-comuni) — Pipeline for SIOPE municipal cash flows 2021-2025 (entrate/uscite) with DuckDB mart and analytical notebooks. `Jupyter Notebook`
- [dataciviclab/openbdap-saldi-storico-stato](https://github.com/dataciviclab/openbdap-saldi-storico-stato) — Historical analysis of State fiscal balances from OpenBDAP — does current spending structurally compress investments? `Jupyter Notebook`
- [dataciviclab/progetto-pilota](https://github.com/dataciviclab/progetto-pilota) — Pilot analysis on Italian municipalities: do those improving recycling rates also reduce total waste? `Jupyter Notebook`

### Normativa / Legal Texts

[Normattiva](https://www.normattiva.it/) is Italy's official portal for consolidated legislation. Tools below help access, convert, and process Italian legal texts programmatically.

- [ondata/normattiva_2_md](https://github.com/ondata/normattiva_2_md) — Convert Italian legislation from Normattiva into clean Markdown format, optimized for AI/LLM consumption. `Python`

### Open Data Portals & Semantic Assets

Italy maintains national open data portals and a set of semantic assets (ontologies, controlled vocabularies) used to standardize data exchange across public administrations.

- [italia/dati-semantic-assets](https://github.com/italia/dati-semantic-assets) — National semantic resources: ontologies and controlled vocabularies for Italian PA. `Python`
- [italia/covid19-opendata-vaccini](https://github.com/italia/covid19-opendata-vaccini) — Open data on COVID-19 vaccine delivery and administration in Italy. `Data`
- [italia/dati.gov.it](https://github.com/italia/dati.gov.it) — Source of dati.gov.it, the Italian government open data portal. `Docs`
- [italia/anpr-opendata](https://github.com/italia/anpr-opendata) — Open data extracted from ANPR (civil registry). `Data`
- [italia/public-opendata-sources](https://github.com/italia/public-opendata-sources) — A comprehensive list of Italian public open data sources. `Python`
- [italia/ckan-it](https://github.com/italia/ckan-it) — Docker images for CKAN with Italian open data extensions. `Shell`
- [italia/pdnd-opendata](https://github.com/italia/pdnd-opendata) — Open data from PDND (Piattaforma Digitale Nazionale Dati). `Data`
- [italia/dati-semantic-mcp](https://github.com/italia/dati-semantic-mcp) — MCP server for interacting with schema.gov.it semantic assets. `TypeScript`
- [ondata/ckan-mcp-server](https://github.com/ondata/ckan-mcp-server) — MCP server for querying CKAN open data portals (package search, DataStore SQL, organizations, groups, tags). `TypeScript`
- [ondata/istat_mcp_server](https://github.com/ondata/istat_mcp_server) — MCP server for interacting with ISTAT SDMX statistical APIs. `Python`
- [dataciviclab/toolkit](https://github.com/dataciviclab/toolkit) — Reproducible data-pipeline engine (RAW → CLEAN → MART) driven by `dataset.yml`, with validation, tracking, and notebook-friendly outputs. `Python`
- [dataciviclab/source-observatory](https://github.com/dataciviclab/source-observatory) — Intelligence layer for Italian public data sources: radar, catalog-watch, resource monitoring, source-check workflows. `Python`
- [dataciviclab/data-explorer](https://github.com/dataciviclab/data-explorer) — Public data frontend built on Observable Framework, DuckDB, and clean Parquet on GCS. `Python`
- [dataciviclab/dataciviclab](https://github.com/dataciviclab/dataciviclab) — Public hub of the DataCivicLab ecosystem — civic data analysis on Italy. `Jupyter Notebook`

---

## 🏥 Healthcare

### FSE (Fascicolo Sanitario Elettronico)

[FSE](https://www.fascicolosanitario.gov.it/) (Fascicolo Sanitario Elettronico) is Italy's Electronic Health Record system, providing citizens with unified access to their medical history across the national healthcare system.

- [italia/design-fse-ui-kit](https://github.com/italia/design-fse-ui-kit) — UI Kit prototypes for the Fascicolo Sanitario Elettronico. `Design`
- [italia/design-fse-eds-ui-kit](https://github.com/italia/design-fse-eds-ui-kit) — UI Kit for the EDS (Ecosistema Dati Sanitari) component of FSE. `Design`

### Tessera Sanitaria

The [Tessera Sanitaria](https://sistemats1.sanita.finanze.it/) (Health Insurance Card) system is used for healthcare expense reporting to the tax authority (Sistema TS). Developers integrate with it to submit medical expenses electronically.

- [francescm/tessera_sanitaria](https://github.com/francescm/tessera_sanitaria) — Read RFID public data from Italian health insurance cards. `Ruby`
- [padosoft/tessera-sanitaria](https://github.com/padosoft/tessera-sanitaria) — Export medical expenses in XML format for Sistema TS. `PHP`

---

## 🎨 Design & UI

### Bootstrap Italia / Design System

[Bootstrap Italia](https://italia.github.io/bootstrap-italia/) is the official Bootstrap 5 theme compliant with the Italian PA design guidelines ("Linee Guida di Design"). It provides accessible, standardized UI components for public-facing services.

- [italia/bootstrap-italia](https://github.com/italia/bootstrap-italia) — Official Bootstrap 5 theme for Italian PA websites. `SCSS`
- [italia/design-react-kit](https://github.com/italia/design-react-kit) — React component library based on Bootstrap Italia. `TypeScript`
- [italia/designers.italia.it](https://github.com/italia/designers.italia.it) — Designers Italia — design resources and knowledge base for Italian PA. `Docs`
- [italia/design-web-toolkit](https://github.com/italia/design-web-toolkit) — Original web UI toolkit (deprecated, use Bootstrap Italia). `HTML` ⚠️ *deprecated*
- [pagopa/mui-italia](https://github.com/pagopa/mui-italia) — Material-UI theme inspired by Bootstrap Italia. `TypeScript`
- [INPS-it/sirio-kit-web](https://github.com/INPS-it/sirio-kit-web) — Sirio Design System — INPS official UI component library. `HTML`

### Framework Integrations

- [italia/design-django-theme](https://github.com/italia/design-django-theme) — Bootstrap Italia template for Django. `Python`
- [italia/design-laravel-theme](https://github.com/italia/design-laravel-theme) — Bootstrap Italia integration for Laravel. `PHP`
- [italia/design-wordpress-theme](https://github.com/italia/design-wordpress-theme) — WordPress theme implementing Bootstrap Italia. `PHP`
- [italia/design-wordpress-theme-italiaWP2](https://github.com/italia/design-wordpress-theme-italiaWP2) — Updated WordPress theme for Italian PA based on Bootstrap Italia. `PHP`
- [italia/design-drupal-theme](https://github.com/italia/design-drupal-theme) — Bootstrap Italia theme for Drupal. `Twig`
- [italia/hugo-theme-bootstrap-italia](https://github.com/italia/hugo-theme-bootstrap-italia) — Hugo theme built with Bootstrap Italia. `HTML` ⚠️ *unmaintained*
- [italia/design-shibboleth-idp-theme](https://github.com/italia/design-shibboleth-idp-theme) — Bootstrap Italia theme for Shibboleth IdP. `JavaScript`
- [italia/design-italia-gatsby-starterkit](https://github.com/italia/design-italia-gatsby-starterkit) — Gatsby starter using Design React Kit. `JavaScript`
- [italia/design-italia-nextjs-starterkit](https://github.com/italia/design-italia-nextjs-starterkit) — Next.js starter using Design React Kit. `TypeScript`
- [italia/design-italia-astro-starterkit](https://github.com/italia/design-italia-astro-starterkit) — Astro starter using Bootstrap Italia. `Astro`
- [albx/bitblazor](https://github.com/albx/bitblazor) — Blazor UI components based on Bootstrap Italia. `C#`

---

## 🔗 Multi-service SDKs & Platforms

### IO App / pagoPA

[IO](https://io.italia.it/) is Italy's official app for public services. Built by [pagoPA](https://www.pagopa.it/), it integrates payments, messages, and digital identity in a single mobile app.

- [pagopa/io-app](https://github.com/pagopa/io-app) — IO app — Italy's public services mobile app. `TypeScript`
- [pagopa/io-backend](https://github.com/pagopa/io-backend) — Backend for the IO app. `TypeScript`
- [pagopa/io-wallet](https://github.com/pagopa/io-wallet) — IT-Wallet provider implementation for IO. `TypeScript`
- [pagopa/io-react-native-wallet](https://github.com/pagopa/io-react-native-wallet) — React Native SDK for IO Wallet attestations. `TypeScript`
- [pagopa/io-app-design-system](https://github.com/pagopa/io-app-design-system) — Component library for IO app. `TypeScript`
- [pagopa/io-ts-commons](https://github.com/pagopa/io-ts-commons) — Common TypeScript utilities for IO. `TypeScript`
- [pagopa/openapi-codegen-ts](https://github.com/pagopa/openapi-codegen-ts) — OpenAPI TypeScript code generator used by IO. `TypeScript`
- [pagopa/pagopa-api](https://github.com/pagopa/pagopa-api) — pagoPA API schemas (XSD/WSDL). `Schemas`
### PDND (Piattaforma Digitale Nazionale Dati)

[PDND](https://www.interop.pagopa.it/) (Piattaforma Digitale Nazionale Dati) is Italy's national data interoperability platform. It enables secure API-to-API communication between public administrations through e-service publishing, voucher-based authentication, and a shared catalog.

- [pagopa/pdnd-interop-frontend](https://github.com/pagopa/pdnd-interop-frontend) — Frontend for the PDND Interoperability platform. `TypeScript`
- [pagopa/interop-public-catalog](https://github.com/pagopa/interop-public-catalog) — Public catalog of PDND e-services. `TypeScript`
- [italia/pdnd-client-assertion-generator](https://github.com/italia/pdnd-client-assertion-generator) — .NET client assertion generator for PDND API authentication. `C#`
- [italia/daf-dataportal](https://github.com/italia/daf-dataportal) — Frontend for the PDND data portal (formerly DAF). `JavaScript`
- [italia/daf-kylo](https://github.com/italia/daf-kylo) — Kylo integration with PDND for data ingestion pipelines. `Java`

### Developers Italia

[Developers Italia](https://developers.italia.it/) is the Italian government's developer community. It hosts the public software catalog and provides tools for publishing and discovering PA open-source projects.

- [italia/developers.italia.it](https://github.com/italia/developers.italia.it) — The Developers Italia website and community portal. `HTML`
- [italia/publiccode-editor](https://github.com/italia/publiccode-editor) — Web editor for creating publiccode.yml files. `TypeScript`
- [italia/publiccode-parser-go](https://github.com/italia/publiccode-parser-go) — publiccode.yml parser and validator. `Go`
- [italia/publiccode-crawler](https://github.com/italia/publiccode-crawler) — Crawler for the Developers Italia open-source catalog. `Go`
- [italia/developers-italia-api](https://github.com/italia/developers-italia-api) — API for the Developers Italia software collection. `Go`

---

## Contributing

Contributions are welcome! Please read the [contribution guidelines](CONTRIBUTING.md) before submitting a PR.

## Maintainers

This list is curated and maintained by [Stefano Salvucci](https://www.stefanosalvucci.com/).

## License

[![CC0](https://licensebuttons.net/p/zero/1.0/88x31.png)](https://creativecommons.org/publicdomain/zero/1.0/)

To the extent possible under law, the maintainers have waived all copyright and related rights to this work.
