# dconp

A DC Object Notation (DCON) parser for the DC programming language.

```dcon
const []const char base = "github.com/you";

dpm::v1::Project {
    name = "game",
    version = "0.1.0",
    link = { "SDL3", "m" },
    dependencies = {
        { location = base, version = "1.0.0" },
    },
    products = { { name = "game", kind = Kind::Executable } },
}
```

dpm reads these files through the compiler, against a schema. This library
reads them at run time and without one, so any program can use DCON for its
own configuration and data files.

## Consumer Setup

Add the package to your `project.dcon`:

```dcon
dependencies = {
    { location = "github.com/Personne-admin/dconp", version = "0.1.0" },
},
```

or run `dpm add github.com/Personne-admin/dconp`.
