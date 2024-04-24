# 4PSCop

This repository contains custom rulesets for CodeCops, designed specifically for each BC version. These rules must be respected by all the AL code written within the company.

## Table of Contents

- Introduction
- Usage

## Introduction

CodeCops is a powerful tool for maintaining code quality. However, different BC versions may require different rules and standards. That's where 4PSCop comes in. Our custom rulesets are tailored to each BC version, ensuring optimal code quality regardless of your BC version.

## Usage

To use the 4PS ruleset, simply copy the link to the raw file version of the ruleset for your BC version and paste it into the ```settings.json``` file in your AL project. Make sure to enable the desired CodeCops and set the ```al.enableCodeAnalysis``` and ```al.enableExternalRulesets``` settings to ```true```. Here's an example of how your ```settings.json``` file should look:
    
```json
{
  "al.enableCodeAnalysis": true,
  "al.enableExternalRulesets": true,
  "al.ruleSetPath": "https://raw.githubusercontent.com/4PS-development/4PSCopRules/main/bc233/4ps_general_app_bc233.ruleset.json",
  "al.codeAnalyzers": [
    "${CodeCop}",
    "${UICop}"
  ]
}
```
For test projects, you can use the following settings:

```json
{
  "al.enableCodeAnalysis": true,
  "al.enableExternalRulesets": true,
  "al.ruleSetPath": "https://raw.githubusercontent.com/4PS-development/4PSCopRules/main/bc233/4ps_general_test_bc233.ruleset.json",
  "al.codeAnalyzers": [
    "${CodeCop}"
  ]
}
```
