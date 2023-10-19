digraph G {
    graph [dpi=300];
    node [shape=ellipse, width=2, height=1.2, style=filled];
    edge [dir=none];

    // Nodes for contexts and identities
    "CULTURAL CONTEXT" [width=5, color=grey];
    "INSTITUTIONAL CONTEXT" [width=4, color=lightgrey];
    "writer/reader" [label="writer\n\n\n\n\n\n\n\nreader", width=3, color=white];
    "Individual/Collective Self" [label="Individual Self\n\n\n\nCollective Self", width=2.5, color=white];
    "Identity Details" [label="autobiographical self\nself as performer\nlinguistic\nargumentative", width=1.5, color=white];

    // Writer's Block as a line cutting through the circles
    "Writer's Block Start" [shape=point, width=0];
    "Writer's Block End" [shape=point, width=0];

    // Defining relations
    "CULTURAL CONTEXT" -> "INSTITUTIONAL CONTEXT" [weight=10];
    "INSTITUTIONAL CONTEXT" -> "writer/reader" [weight=10];
    "writer/reader" -> "Individual/Collective Self" [weight=10];
    "Individual/Collective Self" -> "Identity Details" [weight=10];
    "Writer's Block Start" -> "Writer's Block End" [label="Writer's Block", penwidth=3, color=red];

    // Positioning Writer's Block to cut through the circles
    {
        rank=same;
        "Writer's Block Start";
        "CULTURAL CONTEXT";
    }
}
