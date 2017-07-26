# A list of the kinds of visualisation I want to be able to provide on the ic2s2 data.

## General visualisation

How do I export data to a tool that is easier to visualise so that I can show better labels?

    solution seems to be to use the REST api endpoint, get back a json result, transform that result, and push the transformed result into a suitable tool, like D3.
    See https://neo4j.com/developer/guide-data-visualization/#_howto_graph_visualization_step_by_step for an example and see

    more fine-grained docs on the API are here: https://neo4j.com/docs/developer-manual/current/http-api/#http-api-transactional

    An amazing presentation on viz is here :http://www.apcjones.com/talks/2014-03-26_Neo4j_London/#slide-54

    Another route is to do the data visualisation in a notebook using something like
    https://github.com/graphistry/pygraphistry
    using R as a driver to create netowrk visualisations
    http://christophergandrud.github.io/d3Network/

    

How can I show a graph and omit specific relations, I want to see what it looks like to supress the CoAuthor relation
    The answer is to toggle the "auto-complete" button on the interface, for my purposes, getting a view on the top topics this makes a lot of sense.

How can I just show a count of nodes from a query?

    `MATCH p=()-[r:CoAuthor]->() RETURN count(p)

Another inteesting tool for pluggin in to neo4j 
	https://github.com/neo4j-contrib/neo4j-apoc-procedures `
