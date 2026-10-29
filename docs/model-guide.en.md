# AI Model Setup: Multiple API Profiles and Model Switching

**[English](model-guide.en.md) · [简体中文](model-guide.md) · [Product overview](../README.en.md)**

Model management is available in the report builder settings. The platform can retain multiple OpenAI-compatible API/model profiles and lets users select the active profile through the interface. These captures come from the actual website on 29 October 2026; no additional profiles or keys were invented for the showcase.

## Add and manage API profiles

Open Report builder → Settings → Manage models, then choose Add model. Different providers, model identifiers or purposes can be saved as separate profiles.

![Actual model-management and add-profile window](../assets/model-management.png)

| Field | Purpose |
| --- | --- |
| Display name | A recognizable profile label, for example by intended task |
| Endpoint | The provider's OpenAI-compatible API address |
| Model name | A model identifier actually supported by the provider |
| API key | The user's key, saved separately for each profile; empty in these captures |
| Timeout | The permitted wait time for the request |
| Key application URL and notes | Optional information for maintaining the profile |

The interface offers Save and test and Save and use. Existing profiles can be edited or deleted. Successful calls depend on valid configuration, service availability and model access. The display label is for identification; requests use the configured model identifier.

## Select and switch models

Return to Settings → Generation model. Profiles with an API key appear here; select a profile to make it current. Multiple configurations can be retained independently and selected when needed.

![Actual model selection with current-model marker](../assets/model-selection.png)

The selected profile is used for subsequent model calls. Existing generated content remains saved and is not automatically rewritten merely because the selection changes. Use the relevant generation or regeneration action when an article needs to be processed by the newly selected model.

## Connection to other AI workflows

Report generation, news semantic review at confirmation and enabled AI assistance for regulatory archiving reuse the active API profile. News and regulatory workflows still rely on software evidence validation and controlled changes. Model management does not remove user-confirmation requirements or rule-based fallbacks.

Rule-based paths remain available without an API. Local translation is separate from API configuration. Never post API keys in public feedback; the password fields in these captures are empty.
