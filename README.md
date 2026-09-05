# Global IBAN, BIC/SWIFT & Bank Routing Validator API — .NET / C# SDK

[![NuGet version](https://img.shields.io/nuget/v/StanzaApi.IbanValidator.svg)](https://www.nuget.org/packages/StanzaApi.IbanValidator/)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![Stanza API](https://img.shields.io/badge/Powered%20by-Stanza-blue)](https://stanzaapi.com)

> ISO 13616 MOD-97 IBAN checksum verification, ISO 9362 BIC/SWIFT validation, and national bank routing extraction across 87 countries.

Official high-performance .NET client library for **Global IBAN, BIC/SWIFT & Bank Routing Validator API**, built on the [Stanza Micro-API Network](https://stanzaapi.com). Fully compatible with .NET Standard 2.0, .NET 6.0, .NET 7.0, and .NET 8.0+.

* 🌐 **Online Interactive Sandbox:** [Test your inputs live](https://stanzaapi.com/tools/iban-validator)
* 📚 **API Reference & Schemas:** [View documentation on Stanza](https://stanzaapi.com/tools/iban-validator)
* ⚡ **Platform Overview:** [Explore the Stanza Developer Network](https://stanzaapi.com)

---

## 📦 Installation

```bash
dotnet add package StanzaApi.IbanValidator
```

---

## 🚀 Quickstart

```csharp
using System;
using System.Threading.Tasks;
using StanzaApi.IbanValidator;

class Program
{
    static async Task Main()
    {
        // Initialize client (reads STANZA_API_KEY from environment if not passed)
        var client = new IbanValidatorClient();

        // Perform deterministic verification
        string responseJson = await client.ValidateAsync("DE89370400440532013000");
        Console.WriteLine(responseJson);
    }
}
```

---

## 📄 Example Response

```json
{
  "success": true,
  "data": {
    "valid": true,
    "iban": "DE89370400440532013000",
    "country_code": "DE",
    "bank_code": "37040044",
    "bic_candidate": "COBADEFFXXX"
  }
}
```

---

## ⚙️ Configuration

Pass options directly to the `IbanValidatorClient` constructor:

```csharp
var client = new IbanValidatorClient(
    apiKey: "your_api_key_here",
    baseUrl: "https://stanzaapi.com"
);
```

---

## 🔗 Useful Links

* [Global IBAN, BIC/SWIFT & Bank Routing Validator API Interactive Sandbox](https://stanzaapi.com/tools/iban-validator)
* [Stanza Developer Directory](https://stanzaapi.com)
* [Source Code & Issue Tracker](https://github.com/stanzaapi/iban-validator-csharp)

## 📄 License

MIT © Stanza — Powered by [Stanza](https://stanzaapi.com).
