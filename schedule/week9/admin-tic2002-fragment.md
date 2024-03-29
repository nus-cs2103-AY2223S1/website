{% from "common/macros.njk" import embed_topic, show_as_tab, thumb, timing_badge with context %}
{% from "common/admin.njk" import show_admin_summary with context %}


{% call show_admin_summary() %}
1. Submit the quiz

{{ icon_project }} **Project:**
1. Implement increments `Level-8`,  `A-JavaDoc`, `A-Gradle`, `A-JUnit`
2. Merge branches
{% endcall %}

<!-- ==================================================================================================== -->
{{ heading_project }}
<div id="project">

#### {{ thumb(1) }} Implement increments `Level-8`,  `A-JavaDoc`, `A-Gradle`, `A-JUnit`

<div class="indented">
<include src="dukeFragment.md" boilerplate var-displacement="../.." var-header="**`Level-8`: Dates and Times**" var-fragment="text.md#Level-8" />
<include src="dukeFragment.md" boilerplate var-displacement="../.." var-header="**`A-JavaDoc`: JavaDoc**" var-fragment="extensions-fragment.md#A-JavaDoc" />

<box type="info" seamless>

The `A-Gradle` project increment given below requires you'll need to pull a branch from the [upstream duke repository]({{ url_module_org }}/{{ ip_repo_name }}).<br>
See the panel below on how to pull a branch from another remote repo, but note,

* the remote to pull _from_ is `{{ url_module_org }}/{{ ip_repo_name }}.git` (not `https://github.com/se-edu/samplerepo-things-2.git`)
* the repo to pull _to_ is your local repo used for the project (not `samplerepo-things`)
* the branch to pull is `add-gradle-support`

   {{ embed_topic("../../book/gitAndGithub/pull/text.md#section-working-with-multiple-remotes", "Textbook " + icon_embedding + " Git&Github → Pull → **Wroking with multiple remotes**", "2") }}
</box>

<include src="dukeFragment.md" boilerplate var-displacement="../.." var-header="**`A-Gradle`: Gradle**" var-fragment="extensions-fragment.md#A-Gradle" />

<box type="tip" seamless>

The `A-JUnit` project increment given below can be done using Gradle or without using Gradle. It's easier if you choose to do it using Gradle.
</box>

<include src="dukeFragment.md" boilerplate var-displacement="../.." var-header="**`A-JUnit`: JUnit Testing**" var-fragment="extensions-fragment.md#A-JUnit" />

</div>
<p/>

#### {{ thumb(2) }} Merge branches

<div class="indented">

This task is ==optional but strongly recommended==.

To get a very basic sense of how to use Git in a team project, this exercise simulates a situation where some others are also writing code for your project. Here are the steps.

1. Imagine you are using the GitHub repo {{ url_module_org }}/{{ ip_repo_name }} to collaborate among the team members of your Duke project.

<div class="indented">

<box type="info" seamless>

Although that repo was set up by the teaching team, you could have created one yourself -- all it requires you to do is to create a GitHub organization, create a repository inside it, push your code to it, and add other team members to that GitHub organization.

Alternatively, you could have added the team members as 'collaborators' to your own fork so that they can push code to your fork directly.

</box>
</div>

2. Now, imagine one of the team members have pushed her new code as a branch named `tweak-readme` to the remote repo. Pull that branch and merge it to your `master` branch.
   * See the panel below on how to pull a branch from another remote.
   * In this case, the remote to pull _from_ is `{{ url_module_org }}/{{ ip_repo_name }}.git`, and the repo to pull _to_ is your local repo used for the project.

{{ embed_topic("../../book/gitAndGithub/pull/text.md#section-working-with-multiple-remotes", "Textbook " + icon_embedding + " Git&Github → Pull → **Wroking with multiple remotes**", "2", indent="2") }}

3. Suppose another member has pushed another branch `add-details-to-readme` to the same remote repo. Pull that one too and merge it. If there is a merge conflict, resolve it too.
1. Push your master branch to your fork.

</div>
</div>
