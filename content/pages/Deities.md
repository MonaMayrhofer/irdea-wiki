---
tags:
- General Knowledge
title: Deities
categories:
date: 2023-03-29
lastMod: 2023-04-01
---
{{query (page-tags deity)}}
query-properties:: [:page :pathfinder]
query-sort-by:: pathfinder
query-sort-desc:: true

query-table:: false
{{< logseq/orgQUERY >}}{:title "All pages have a *programming* tag"
 :query [:find (pull ?p [*])
       :in $ ?tag
       :where
       [?t :block/name ?tag]
       [?p :block/tags ?t]
       [?p :block/name ?name]]
 :inputs ["deity"]
:result-transform (fn [result] (reverse (sort-by (fn [it] (get-in it [:block/properties :pathfinder])) result)))
 :view (fn [result]
[:div.table-wrapper
       [:table.table-auto
[:thead
  [:tr
    [:th "Name"]
    [:th "Pathfinder"]
    [:th "God Of"]
  ]
]
[:tbody
        (for [page result]
[:tr 
[:td (let [name (get-in page [:block/name])] [:a {:href (str "#/page/" name)} (clojure.string/capitalize name)])]
[:td (get-in page [:block/properties :pathfinder])]
[:td (get-in page [:block/properties :god-of])]
]
)]]]
)
}
{{< / logseq/orgQUERY >}}





# Phrases

  + Hadur's Hammer be with you

  + One cannot smith without a fire

  + Lock it [a secret] up with the silver key.

# Pathfinder <=> Irdea Gods

  + |Lost Omens|Irdea|
|Abadar||
|Alseta|[[Sorrelja]]|
|Asmodeus| [[Asmodeus]] |
|Brigh|[[Dreifh]]|
|Calistria|[[Solistre]]|
|Cayden Cailean |[[Ayden Alemoth]]|
|Desna|[[Saerna]]|
|Erastril|[[]]|
|Gorum|[[Farbod]]|
|Gozreh|[[Ishran]]|
|Groetus|[[Gournurat]]|
|Iomedae||
|Irori|[[Kalsai]]|
|Lamashtu||
|Milani|[[Laira]]|
|Nethys||
|Norgorber||
|Pharasma|[[Atha]]|
|Rovagug||
|Sarenrae|[[Morrigha]]|
|Shelyn||
|Sivanah|[[Niona]]|
|Torag|[[Haldur]]|
|Urgathoa||
|Zon-Kuthon||

  + 
