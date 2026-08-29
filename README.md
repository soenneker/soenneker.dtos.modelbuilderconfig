[![](https://img.shields.io/nuget/v/soenneker.dtos.modelbuilderconfig.svg?style=for-the-badge)](https://www.nuget.org/packages/soenneker.dtos.modelbuilderconfig/)
[![](https://img.shields.io/github/actions/workflow/status/soenneker/soenneker.dtos.modelbuilderconfig/publish-package.yml?style=for-the-badge)](https://github.com/soenneker/soenneker.dtos.modelbuilderconfig/actions/workflows/publish-package.yml)
[![](https://img.shields.io/nuget/dt/soenneker.dtos.modelbuilderconfig.svg?style=for-the-badge)](https://www.nuget.org/packages/soenneker.dtos.modelbuilderconfig/)
[![](https://img.shields.io/github/actions/workflow/status/soenneker/soenneker.dtos.modelbuilderconfig/codeql.yml?label=CodeQL&style=for-the-badge)](https://github.com/soenneker/soenneker.dtos.modelbuilderconfig/actions/workflows/codeql.yml)

# Soenneker.Dtos.ModelBuilderConfig

Represents the configuration for a machine learning or model-building scenario.

## Install

```bash
dotnet add package Soenneker.Dtos.ModelBuilderConfig
```

## What you get

- `MbConfig` — Represents the configuration for a machine learning or model-building scenario.
- `MbConfigColumnProperty` — Represents metadata and configuration properties for a specific column in a dataset.
- `MbConfigDataSource` — Represents the data source configuration for the model builder, including file and formatting details.
- `MbConfigEnvironment` — Represents environment-specific settings or metadata for the model builder configuration.
- `MbConfigRunHistory` — Represents the run history for a model training session, including trial data and evaluation metrics.
- `MbConfigTrainingOption` — Represents configurable options for training a machine learning model.
- `MbConfigTrial` — Represents a single trial or experiment in a model training run.

## API at a glance

| API | What it does | Result / important behavior |
| --- | --- | --- |
| `MbConfig.Scenario` | Gets or sets the scenario name or identifier for the configuration. | Gets or sets the scenario name or identifier for the configuration. |
| `MbConfig.Type` | Gets or sets the type of configuration or model. | Gets or sets the type of configuration or model. |
| `MbConfig.Version` | Gets or sets the version number of the configuration schema or format. | Gets or sets the version number of the configuration schema or format. |
| `MbConfig.DataSource` | Gets or sets the data source configuration details. | Gets or sets the data source configuration details. |
| `MbConfig.Environment` | Gets or sets the environment settings for the configuration. | Gets or sets the environment settings for the configuration. |
| `MbConfig.TrainingOption` | Gets or sets the training options related to the configuration. | Gets or sets the training options related to the configuration. |
| `MbConfig.RunHistory` | Gets or sets the run history information for previous executions. | Gets or sets the run history information for previous executions. |
| `MbConfigColumnProperty.ColumnName` | Gets or sets the name of the column. | Gets or sets the name of the column. |
| `MbConfigColumnProperty.ColumnPurpose` | Gets or sets the intended purpose of the column (e.g., label, feature, ignore). | Gets or sets the intended purpose of the column (e.g., label, feature, ignore). |
| `MbConfigColumnProperty.ColumnDataFormat` | Gets or sets the format of the data in the column (e.g., numeric, text, datetime). | Gets or sets the format of the data in the column (e.g., numeric, text, datetime). |
| `MbConfigColumnProperty.IsCategorical` | Gets or sets a value indicating whether the column is treated as categorical. | Gets or sets a value indicating whether the column is treated as categorical. |
| `MbConfigColumnProperty.Type` | Gets or sets the type of the column, possibly used for internal classification or processing. | Gets or sets the type of the column, possibly used for internal classification or processing. |
| `MbConfigColumnProperty.Version` | Gets or sets the version number of the column property schema. | Gets or sets the version number of the column property schema. |
| `MbConfigDataSource.Type` | Gets or sets the type of data source (e.g., "csv", "json", etc.). | Gets or sets the type of data source (e.g., "csv", "json", etc.). |
| `MbConfigDataSource.Version` | Gets or sets the version of the data source configuration schema. | Gets or sets the version of the data source configuration schema. |
| `MbConfigDataSource.FilePath` | Gets or sets the file path to the data source. | Gets or sets the file path to the data source. |
| `MbConfigDataSource.Delimiter` | Gets or sets the delimiter used in the data file (e.g., ",", ";", "\t"). | Gets or sets the delimiter used in the data file (e.g., ",", ";", "\t"). |
| `MbConfigDataSource.DecimalMarker` | Gets or sets the character used as a decimal marker (e.g., ".", ","). | Gets or sets the character used as a decimal marker (e.g., ".", ","). |
