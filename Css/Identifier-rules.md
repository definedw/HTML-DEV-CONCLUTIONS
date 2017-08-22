# Identifier Rules

> Declaration:All the rules just apply to my-project!

Recently,I wanna build new structure HTML Render Tree.

Here is the result of my attempt.

### Portrait

* primary   


    ```text
    -- container
      -- header
      -- content
      -- footer
    ```

* middle


    ```text
    -- container
        -- header
            -- {block}
                -- {block}-{modify}
                -- {modify}
        -- content
            -- similar to header
        -- footer
            -- similar to header
    ```

* higher


```text
-- container
    -- header
        // only sign {hd},if nest more than two pair
        --hd-{block} || hd-{block}&&{modify}
            // only sign {head},if more than three pair
            -- head-{block}
                -- header-{block} || head-{block}&&{modify}
                -- {modify}
     -- content
            -- similar to header
        -- footer
            -- similar to header
```


###  Landscape

* primary


```text
-- container
    -- left
    -- middle
    -- right
```

* middle


```text
-- container
    -- left
        -- lt-{block}
            -- {modify}
    -- middle
        -- similar to left
    -- right
        -- similar to left
```

* higher


```text
-- container
    -- left
        // register only sign in header such as {lt}/{left}
        -- lt-{block}
            -- {modify}
```


