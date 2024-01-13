---

database-plugin: basic

---
# DB Cars

```yaml:dbfolder
name: Cars
description: Fun cars with good value for money. Source of inspiration for future purchases.
columns:
  __file__:
    key: __file__
    id: __file__
    input: markdown
    label: File
    accessorKey: __file__
    isMetadata: true
    skipPersist: false
    isDragDisabled: false
    csvCandidate: true
    position: 1
    isHidden: false
    sortIndex: -1
    config:
      enable_media_view: true
      link_alias_enabled: true
      media_width: 100
      media_height: 100
      isInline: true
      task_hide_completed: true
      footer_type: none
      persist_changes: false
      content_alignment: text-align-left
      content_vertical_alignment: align-middle
  Moteur:
    input: text
    accessorKey: Moteur
    key: Moteur
    id: Moteur
    label: Moteur
    position: 4
    skipPersist: false
    isHidden: false
    sortIndex: -1
    config:
      enable_media_view: true
      link_alias_enabled: true
      media_width: 100
      media_height: 100
      isInline: false
      task_hide_completed: true
      footer_type: none
      persist_changes: false
      wrap_content: true
  Poids:
    input: text
    accessorKey: Poids
    key: Poids
    id: Poids
    label: Poids
    position: 7
    skipPersist: false
    isHidden: false
    sortIndex: -1
    config:
      enable_media_view: true
      link_alias_enabled: true
      media_width: 100
      media_height: 100
      isInline: false
      task_hide_completed: true
      footer_type: none
      persist_changes: false
  Puissance:
    input: text
    accessorKey: Puissance
    key: Puissance
    id: Puissance
    label: Puissance
    position: 8
    skipPersist: false
    isHidden: false
    sortIndex: -1
    isSorted: false
    isSortedDesc: false
    config:
      enable_media_view: true
      link_alias_enabled: true
      media_width: 100
      media_height: 100
      isInline: false
      task_hide_completed: true
      footer_type: none
      persist_changes: false
      wrap_content: true
  Torque:
    input: text
    accessorKey: Torque
    key: Torque
    id: Torque
    label: Couple
    position: 9
    skipPersist: false
    isHidden: false
    sortIndex: -1
    width: 140
    config:
      enable_media_view: true
      link_alias_enabled: true
      media_width: 100
      media_height: 100
      isInline: false
      task_hide_completed: true
      footer_type: none
      persist_changes: false
      wrap_content: true
  Price_range:
    input: text
    accessorKey: Price_range
    key: Price_range
    id: Price_range
    label: Côte
    position: 2
    skipPersist: false
    isHidden: false
    sortIndex: -1
    config:
      enable_media_view: true
      link_alias_enabled: true
      media_width: 100
      media_height: 100
      isInline: false
      task_hide_completed: true
      footer_type: none
      persist_changes: false
      wrap_content: true
  Production_years:
    input: text
    accessorKey: Production_years
    key: Production_years
    id: Production_years
    label: Millésimes
    position: 3
    skipPersist: false
    isHidden: false
    sortIndex: -1
    width: 62
    config:
      enable_media_view: true
      link_alias_enabled: true
      media_width: 100
      media_height: 100
      isInline: false
      task_hide_completed: true
      footer_type: none
      persist_changes: false
      wrap_content: true
  V_max:
    input: text
    accessorKey: V_max
    key: V_max
    id: V_max
    label: V max
    position: 16
    skipPersist: false
    isHidden: false
    sortIndex: -1
    config:
      enable_media_view: true
      link_alias_enabled: true
      media_width: 100
      media_height: 100
      isInline: false
      task_hide_completed: true
      footer_type: none
      persist_changes: false
  Boîte:
    input: text
    accessorKey: Boîte
    key: Boîte
    id: Boîte
    label: Boîte
    position: 5
    skipPersist: false
    isHidden: false
    sortIndex: -1
    width: 77
    config:
      enable_media_view: true
      link_alias_enabled: true
      media_width: 100
      media_height: 100
      isInline: false
      task_hide_completed: true
      footer_type: none
      persist_changes: false
      wrap_content: true
  0_à_100_km/h:
    input: text
    accessorKey: 0_à_100_km/h
    key: 0_à_100_km/h
    id: 0_à_100_km/h
    label: 0 à 100
    position: 15
    skipPersist: false
    isHidden: false
    sortIndex: -1
    config:
      enable_media_view: true
      link_alias_enabled: true
      media_width: 100
      media_height: 100
      isInline: false
      task_hide_completed: true
      footer_type: none
      persist_changes: false
  Pneus_AV:
    input: text
    accessorKey: Pneus_AV
    key: Pneus_AV
    id: Pneus_AV
    label: Pneus AV
    position: 23
    skipPersist: false
    isHidden: false
    sortIndex: -1
    config:
      enable_media_view: true
      link_alias_enabled: true
      media_width: 100
      media_height: 100
      isInline: false
      task_hide_completed: true
      footer_type: none
      persist_changes: false
      wrap_content: true
  Pneus_AR:
    input: text
    accessorKey: Pneus_AR
    key: Pneus_AR
    id: Pneus_AR
    label: Pneus AR
    position: 24
    skipPersist: false
    isHidden: false
    sortIndex: -1
    config:
      enable_media_view: true
      link_alias_enabled: true
      media_width: 100
      media_height: 100
      isInline: false
      task_hide_completed: true
      footer_type: none
      persist_changes: false
      wrap_content: true
  Dimensions:
    input: text
    accessorKey: Dimensions
    key: Dimensions
    id: Dimensions
    label: L x l x h
    position: 25
    skipPersist: false
    isHidden: false
    sortIndex: -1
    width: 173
    config:
      enable_media_view: true
      link_alias_enabled: true
      media_width: 100
      media_height: 100
      isInline: false
      task_hide_completed: true
      footer_type: none
      persist_changes: false
      wrap_content: true
  Rapport_PP:
    input: text
    accessorKey: Rapport_PP
    key: Rapport_PP
    id: Rapport_PP
    label: Poids/Puissance
    position: 10
    skipPersist: false
    isHidden: false
    sortIndex: -1
    config:
      enable_media_view: true
      link_alias_enabled: true
      media_width: 100
      media_height: 100
      isInline: false
      task_hide_completed: true
      footer_type: none
      persist_changes: false
  Rapport_PC:
    input: text
    accessorKey: Rapport_PC
    key: Rapport_PC
    id: Rapport_PC
    label: Poids/Couple
    position: 11
    skipPersist: false
    isHidden: false
    sortIndex: -1
    config:
      enable_media_view: true
      link_alias_enabled: true
      media_width: 100
      media_height: 100
      isInline: false
      task_hide_completed: true
      footer_type: none
      persist_changes: false
  newColumn15:
    input: text
    accessorKey: newColumn15
    key: newColumn15
    id: newColumn15
    label: Empattement
    position: 26
    skipPersist: false
    isHidden: false
    sortIndex: -1
    config:
      enable_media_view: true
      link_alias_enabled: true
      media_width: 100
      media_height: 100
      isInline: false
      task_hide_completed: true
      footer_type: none
      persist_changes: false
  newColumn16:
    input: text
    accessorKey: newColumn16
    key: newColumn16
    id: newColumn16
    label: Alésage
    position: 13
    skipPersist: false
    isHidden: false
    sortIndex: -1
    config:
      enable_media_view: true
      link_alias_enabled: true
      media_width: 100
      media_height: 100
      isInline: false
      task_hide_completed: true
      footer_type: none
      persist_changes: false
  Conso:
    input: text
    accessorKey: Conso
    key: Conso
    id: Conso
    label: Conso
    position: 18
    skipPersist: false
    isHidden: false
    sortIndex: -1
    config:
      enable_media_view: true
      link_alias_enabled: true
      media_width: 100
      media_height: 100
      isInline: false
      task_hide_completed: true
      footer_type: none
      persist_changes: false
      wrap_content: true
  C02:
    input: text
    accessorKey: C02
    key: C02
    id: C02
    label: C02
    position: 17
    skipPersist: false
    isHidden: false
    sortIndex: -1
    config:
      enable_media_view: true
      link_alias_enabled: true
      media_width: 100
      media_height: 100
      isInline: false
      task_hide_completed: true
      footer_type: none
      persist_changes: false
  newColumn20:
    input: text
    accessorKey: newColumn20
    key: newColumn20
    id: newColumn20
    label: Course
    position: 14
    skipPersist: false
    isHidden: false
    sortIndex: -1
    config:
      enable_media_view: true
      link_alias_enabled: true
      media_width: 100
      media_height: 100
      isInline: false
      task_hide_completed: true
      footer_type: none
      persist_changes: false
  newColumn22:
    input: text
    accessorKey: newColumn22
    key: newColumn22
    id: newColumn22
    label: Transmission
    position: 6
    skipPersist: false
    isHidden: false
    sortIndex: -1
    config:
      enable_media_view: true
      link_alias_enabled: true
      media_width: 100
      media_height: 100
      isInline: false
      task_hide_completed: true
      footer_type: none
      persist_changes: false
  newColumn23:
    input: text
    accessorKey: newColumn23
    key: newColumn23
    id: newColumn23
    label: Budget 1000 km
    position: 22
    skipPersist: false
    isHidden: false
    sortIndex: -1
    width: 144
    config:
      enable_media_view: true
      link_alias_enabled: true
      media_width: 100
      media_height: 100
      isInline: false
      task_hide_completed: true
      footer_type: none
      persist_changes: false
  newColumn24:
    input: text
    accessorKey: newColumn24
    key: newColumn24
    id: newColumn24
    label: Réservoir
    position: 19
    skipPersist: false
    isHidden: false
    sortIndex: -1
    config:
      enable_media_view: true
      link_alias_enabled: true
      media_width: 100
      media_height: 100
      isInline: false
      task_hide_completed: true
      footer_type: none
      persist_changes: false
  newColumn26:
    input: text
    accessorKey: newColumn26
    key: newColumn26
    id: newColumn26
    label: Budget Plein
    position: 21
    skipPersist: false
    isHidden: false
    sortIndex: -1
    width: 115
    config:
      enable_media_view: true
      link_alias_enabled: true
      media_width: 100
      media_height: 100
      isInline: false
      task_hide_completed: true
      footer_type: none
      persist_changes: false
  newColumn27:
    input: text
    accessorKey: newColumn27
    key: newColumn27
    id: newColumn27
    label: Rendement
    position: 12
    skipPersist: false
    isHidden: false
    sortIndex: -1
    config:
      enable_media_view: true
      link_alias_enabled: true
      media_width: 100
      media_height: 100
      isInline: false
      task_hide_completed: true
      footer_type: none
      persist_changes: false
      wrap_content: true
  newColumn25:
    input: text
    accessorKey: newColumn25
    key: newColumn25
    id: newColumn25
    label: Autonomie
    position: 20
    skipPersist: false
    isHidden: false
    sortIndex: -1
    config:
      enable_media_view: true
      link_alias_enabled: true
      media_width: 100
      media_height: 100
      isInline: true
      task_hide_completed: true
      footer_type: none
      persist_changes: false
  Coffre:
    input: text
    accessorKey: Coffre
    key: Coffre
    id: Coffre
    label: Coffre
    position: 27
    skipPersist: false
    isHidden: false
    sortIndex: -1
    config:
      enable_media_view: true
      link_alias_enabled: true
      media_width: 100
      media_height: 100
      isInline: true
      task_hide_completed: true
      footer_type: none
      persist_changes: false
  newColumn28:
    input: text
    accessorKey: newColumn28
    key: newColumn28
    id: newColumn28
    label: Budget 4 pneus
    position: 25
    skipPersist: false
    isHidden: false
    sortIndex: -1
    config:
      enable_media_view: true
      link_alias_enabled: true
      media_width: 100
      media_height: 100
      isInline: true
      task_hide_completed: true
      footer_type: none
      persist_changes: false
config:
  remove_field_when_delete_column: false
  cell_size: wide
  sticky_first_column: true
  group_folder_column: 
  remove_empty_folders: false
  automatically_group_files: false
  hoist_files_with_empty_attributes: true
  show_metadata_created: false
  show_metadata_modified: false
  show_metadata_tasks: false
  show_metadata_inlinks: false
  show_metadata_outlinks: false
  show_metadata_tags: false
  source_data: current_folder
  source_form_result: 
  source_destination_path: /
  row_templates_folder: /
  current_row_template: 
  pagination_size: 10
  font_size: 12
  enable_js_formulas: false
  formula_folder_path: /
  inline_default: true
  inline_new_position: last_field
  date_format: yyyy-MM-dd
  datetime_format: "yyyy-MM-dd HH:mm:ss"
  metadata_date_format: "yyyy-MM-dd HH:mm:ss"
  enable_footer: false
  implementation: default
filters:
  enabled: false
  conditions:
```