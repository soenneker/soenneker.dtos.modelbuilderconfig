[![](https://img.shields.io/nuget/v/soenneker.dtos.modelbuilderconfig.svg?style=for-the-badge)](https://www.nuget.org/packages/soenneker.dtos.modelbuilderconfig/)
[![](https://img.shields.io/github/actions/workflow/status/soenneker/soenneker.dtos.modelbuilderconfig/publish-package.yml?style=for-the-badge)](https://github.com/soenneker/soenneker.dtos.modelbuilderconfig/actions/workflows/publish-package.yml)
[![](https://img.shields.io/nuget/dt/soenneker.dtos.modelbuilderconfig.svg?style=for-the-badge)](https://www.nuget.org/packages/soenneker.dtos.modelbuilderconfig/)
[![](https://img.shields.io/github/actions/workflow/status/soenneker/soenneker.dtos.modelbuilderconfig/codeql.yml?label=CodeQL&style=for-the-badge)](https://github.com/soenneker/soenneker.dtos.modelbuilderconfig/actions/workflows/codeql.yml)

# Soenneker.Dtos.ModelBuilderConfig

`System.Text.Json` DTOs for reading and writing ML.NET Model Builder configuration files, including the data source, training options, validation strategy, and recorded trials.

## Install

```bash
dotnet add package Soenneker.Dtos.ModelBuilderConfig
```

## Read a configuration

```csharp
using System.Text.Json;
using Soenneker.Dtos.ModelBuilderConfig;

string json = await File.ReadAllTextAsync("ModelBuilder.mbconfig");
MbConfig? config = JsonSerializer.Deserialize<MbConfig>(json);

if (config?.TrainingOption is { } training)
{
    Console.WriteLine($"Label: {training.LabelColumn}");
    Console.WriteLine($"Metric: {training.OptimizeMetric}");
    Console.WriteLine($"Time limit: {training.TrainingTime} seconds");
}
```

The models preserve Model Builder's PascalCase JSON property names such as `DataSource`, `TrainingOption`, and `RunHistory`.

## Model map

- `MbConfig` is the root document.
- `MbConfigDataSource` describes the input file, delimiter, decimal marker, and columns.
- `MbConfigTrainingOption` describes trainers, target column, metric, time limit, seed, and validation.
- `MbConfigEnvironment` carries the environment type and schema version.
- `MbConfigRunHistory` and `MbConfigTrial` expose prior trial results.

These are mutable serialization models. String values such as scenario, trainer, metric, and validation type are passed through as-is; the package does not validate them against a particular Model Builder version. Nullable collections may remain `null` when their JSON members are absent, so check them before enumeration.
