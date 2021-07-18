---
title: Control flow
category: Reference Guides / API Reference
---

# Control flow

By default, Streamlit apps execute the script entirely, but we allow some functionality to handle control flow in your applications.

<Autofunction function="streamlit.stop" />

# Add widgets to sidebar

Not only can you add interactivity to your report with widgets, you can organize them into a sidebar with `st.sidebar.[element_name]`. Each element that's passed to `st.sidebar` is pinned to the left, allowing users to focus on the content in your app. The only elements that aren't supported are `st.echo` and `st.spinner`.

Here's an example of how you'd add a selectbox to your sidebar.

```python
import streamlit as st

add_selectbox = st.sidebar.selectbox(
    "How would you like to be contacted?",
    ("Email", "Home phone", "Mobile phone")
)
```