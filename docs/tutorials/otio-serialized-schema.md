# Serialized Data Documentation

This documents all the OpenTimelineIO classes that serialize to and from JSON,
omitting SchemaDef plugins.

This document is automatically generated by running
 docs/autogen_serialized_datamodel.py, or by running `make doc-model`.  It is
 part of the unit tests suite and should be updated whenever the schema changes.
 If it needs to be updated, run: `make doc-model-update` and this file should be
 regenerated.

# Class Documentation


## Module: opentimelineio.adapters

### Adapter.1

*full module path*: `opentimelineio.adapters.Adapter`

*documentation*:

```
Adapters convert between OTIO and other formats.

    Note that this class is not subclassed by adapters.  Rather, an adapter is
    a python module that implements at least one of the following functions:

        write_to_string(input_otio)
        write_to_file(input_otio, filepath) (optionally inferred)
        read_from_string(input_str)
        read_from_file(filepath) (optionally inferred)

    ...as well as a small json file that advertises the features of the adapter
    to OTIO.  This class serves as the wrapper around these modules internal
    to OTIO.  You should not need to extend this class to create new adapters
    for OTIO.

    For more information:
    https://opentimelineio.readthedocs.io/en/latest/tutorials/write-an-adapter.html# # noqa
    
```

parameters:
- *execution_scope*: Describes whether this adapter is executed in the current python process or in a subshell.  Options are: ['in process', 'out of process'].
- *filepath*: Absolute path or relative path to adapter module from location of json.
- *name*: Adapter name.
- *suffixes*: File suffixes associated with this adapter.

## Module: opentimelineio.core

### Composable.1

*full module path*: `opentimelineio.core.Composable`

*documentation*:

```
None
```

parameters:
- *metadata*: 
- *name*: 

### Composition.1

*full module path*: `opentimelineio.core.Composition`

*documentation*:

```
None
```

parameters:
- *effects*: 
- *markers*: 
- *metadata*: 
- *name*: 
- *source_range*: 

### Item.1

*full module path*: `opentimelineio.core.Item`

*documentation*:

```
None
```

parameters:
- *effects*: 
- *markers*: 
- *metadata*: 
- *name*: 
- *source_range*: 

### MediaReference.1

*full module path*: `opentimelineio.core.MediaReference`

*documentation*:

```
None
```

parameters:
- *available_range*: 
- *metadata*: 
- *name*: 

### SerializableObjectWithMetadata.1

*full module path*: `opentimelineio.core.SerializableObjectWithMetadata`

*documentation*:

```
None
```

parameters:
- *metadata*: 
- *name*: 

## Module: opentimelineio.hooks

### HookScript.1

*full module path*: `opentimelineio.hooks.HookScript`

*documentation*:

```
None
```

parameters:
- *execution_scope*: Describes whether this adapter is executed in the current python process or in a subshell.  Options are: ['in process', 'out of process'].
- *filepath*: Absolute path or relative path to adapter module from location of json.
- *name*: Adapter name.

## Module: opentimelineio.media_linker

### MediaLinker.1

*full module path*: `opentimelineio.media_linker.MediaLinker`

*documentation*:

```
None
```

parameters:
- *execution_scope*: Describes whether this adapter is executed in the current python process or in a subshell.  Options are: ['in process', 'out of process'].
- *filepath*: Absolute path or relative path to adapter module from location of json.
- *name*: Adapter name.

## Module: opentimelineio.opentime

### RationalTime.1

*full module path*: `opentimelineio.opentime.RationalTime`

*documentation*:

```
None
```

parameters:
- *rate*: 
- *value*: 

### TimeRange.1

*full module path*: `opentimelineio.opentime.TimeRange`

*documentation*:

```
None
```

parameters:
- *duration*: 
- *start_time*: 

### TimeTransform.1

*full module path*: `opentimelineio.opentime.TimeTransform`

*documentation*:

```
None
```

parameters:
- *offset*: 
- *rate*: 
- *scale*: 

## Module: opentimelineio.plugins

### PluginManifest.1

*full module path*: `opentimelineio.plugins.Manifest`

*documentation*:

```
Defines an OTIO plugin Manifest.

    This is an internal OTIO implementation detail.  A manifest tracks a
    collection of adapters and allows finding specific adapters by suffix

    For writing your own adapters, consult:
        https://opentimelineio.readthedocs.io/en/latest/tutorials/write-an-adapter.html#
    
```

parameters:
- *adapters*: Adapters this manifest describes.
- *hook_scripts*: Scripts that can be attached to hooks.
- *hooks*: Hooks that hooks scripts can be attached to.
- *media_linkers*: Media Linkers this manifest describes.
- *schemadefs*: Schemadefs this manifest describes.

### SerializableObject.1

*full module path*: `opentimelineio.plugins.PythonPlugin`

*documentation*:

```
A class of plugin that is encoded in a python module, exposed via a
    manifest.
    
```

parameters:
- *execution_scope*: Describes whether this adapter is executed in the current python process or in a subshell.  Options are: ['in process', 'out of process'].
- *filepath*: Absolute path or relative path to adapter module from location of json.
- *name*: Adapter name.

## Module: opentimelineio.schema

### Clip.1

*full module path*: `opentimelineio.schema.Clip`

*documentation*:

```
None
```

parameters:
- *effects*: 
- *markers*: 
- *media_reference*: 
- *metadata*: 
- *name*: 
- *source_range*: 

### Effect.1

*full module path*: `opentimelineio.schema.Effect`

*documentation*:

```
None
```

parameters:
- *effect_name*: 
- *metadata*: 
- *name*: 

### ExternalReference.1

*full module path*: `opentimelineio.schema.ExternalReference`

*documentation*:

```
None
```

parameters:
- *available_range*: 
- *metadata*: 
- *name*: 
- *target_url*: 

### FreezeFrame.1

*full module path*: `opentimelineio.schema.FreezeFrame`

*documentation*:

```
None
```

parameters:
- *effect_name*: 
- *metadata*: 
- *name*: 
- *time_scalar*: 

### Gap.1

*full module path*: `opentimelineio.schema.Gap`

*documentation*:

```
None
```

parameters:
- *effects*: 
- *markers*: 
- *metadata*: 
- *name*: 
- *source_range*: 

### GeneratorReference.1

*full module path*: `opentimelineio.schema.GeneratorReference`

*documentation*:

```
None
```

parameters:
- *available_range*: 
- *generator_kind*: 
- *metadata*: 
- *name*: 
- *parameters*: 

### LinearTimeWarp.1

*full module path*: `opentimelineio.schema.LinearTimeWarp`

*documentation*:

```
None
```

parameters:
- *effect_name*: 
- *metadata*: 
- *name*: 
- *time_scalar*: 

### Marker.2

*full module path*: `opentimelineio.schema.Marker`

*documentation*:

```
None
```

parameters:
- *color*: 
- *marked_range*: 
- *metadata*: 
- *name*: 

### MissingReference.1

*full module path*: `opentimelineio.schema.MissingReference`

*documentation*:

```
None
```

parameters:
- *available_range*: 
- *metadata*: 
- *name*: 

### SerializableCollection.1

*full module path*: `opentimelineio.schema.SerializableCollection`

*documentation*:

```
None
```

parameters:
- *metadata*: 
- *name*: 

### Stack.1

*full module path*: `opentimelineio.schema.Stack`

*documentation*:

```
None
```

parameters:
- *effects*: 
- *markers*: 
- *metadata*: 
- *name*: 
- *source_range*: 

### TimeEffect.1

*full module path*: `opentimelineio.schema.TimeEffect`

*documentation*:

```
None
```

parameters:
- *effect_name*: 
- *metadata*: 
- *name*: 

### Timeline.1

*full module path*: `opentimelineio.schema.Timeline`

*documentation*:

```
None
```

parameters:
- *global_start_time*: 
- *metadata*: 
- *name*: 
- *tracks*: 

### Track.1

*full module path*: `opentimelineio.schema.Track`

*documentation*:

```
None
```

parameters:
- *effects*: 
- *kind*: 
- *markers*: 
- *metadata*: 
- *name*: 
- *source_range*: 

### Transition.1

*full module path*: `opentimelineio.schema.Transition`

*documentation*:

```
None
```

parameters:
- *in_offset*: 
- *metadata*: 
- *name*: 
- *out_offset*: 
- *transition_type*: 

### SchemaDef.1

*full module path*: `opentimelineio.schema.SchemaDef`

*documentation*:

```
None
```

parameters:
- *execution_scope*: Describes whether this adapter is executed in the current python process or in a subshell.  Options are: ['in process', 'out of process'].
- *filepath*: Absolute path or relative path to adapter module from location of json.
- *name*: Adapter name.