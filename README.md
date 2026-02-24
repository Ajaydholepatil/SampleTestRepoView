
<!--header-->
<table>
  <tr><td colspan="2"><a href="/README.md#-plugins">← Back to plugins index</a></td></tr>
  <tr><th colspan="2"><h3>🙋 Introduction</h3></th></tr>
  <tr><td colspan="2" align="center"><p>This plugin displays account bio or organization/repository description.</p>
<p>Since account bio is already displayed on account profile, this plugin is mostly intended for external usage.</p>
</td></tr>
  <tr><th>⚠️ Disclaimer</th><td><p>This plugin is not affiliated, associated, authorized, endorsed by, or in any way officially connected with <a href="https://github.com">GitHub</a>.
All product and company names are trademarks™ or registered® trademarks of their respective holders.</p>
</td></tr>
  <tr>
    <th rowspan="3">Supported features<br><sub><a href="metadata.yml">→ Full specification</a></sub></th>
    <td><a href="/source/templates/classic/README.md"><code>📗 Classic template</code></a> <a href="/source/templates/repository/README.md"><code>📘 Repository template</code></a></td>
  </tr>
  <tr>
    <td><code>👤 Users</code> <code>👥 Organizations</code> <code>📓 Repositories</code></td>
  </tr>
  <tr>
    <td><code>🔑 (scopeless)</code> <code>read:org (optional)</code> <code>read:user (optional)</code> <code>read:packages (optional)</code> <code>repo (optional)</code></td>
  </tr>
  <tr>
    <td colspan="2" align="center">
      <details open><summary>For a user or an organization</summary><img src="https://github.com/lowlighter/metrics/blob/examples/metrics.plugin.introduction.svg" alt=""></img></details>
      <details><summary>For a repository</summary><img src="https://github.com/lowlighter/metrics/blob/examples/metrics.plugin.introduction.repository.svg" alt=""></img></details>
      <img width="900" height="1" alt="">
    </td>
  </tr>
</table>
<!--/header-->

## ➡️ Available options

<!--options-->
<table>
  <tr>
    <td align="center" nowrap="nowrap">Option</i></td><td align="center" nowrap="nowrap">Description</td>
  </tr>
  <tr>
    <td nowrap="nowrap"><h4><code>plugin_introduction</code></h4></td>
    <td rowspan="2"><p>Enable introduction plugin</p>
<img width="900" height="1" alt=""></td>
  </tr>
  <tr>
    <td nowrap="nowrap"><b>type:</b> <code>boolean</code>
<br>
<b>default:</b> no<br></td>
  </tr>
  <tr>
    <td nowrap="nowrap"><h4><code>plugin_introduction_title</code></h4></td>
    <td rowspan="2"><p>Section title</p>
<img width="900" height="1" alt=""></td>
  </tr>
  <tr>
    <td nowrap="nowrap"><b>type:</b> <code>boolean</code>
<br>
<b>default:</b> yes<br></td>
  </tr>
</table>
<!--/options-->

## ℹ️ Examples workflows

<!--examples-->
```yaml
name: Organization introduction
uses: lowlighter/metrics@latest
with:
  filename: metrics.plugin.introduction.svg
  token: ${{ secrets.METRICS_TOKEN }}
  user: github
  base: header
  plugin_introduction: yes

```
```yaml
name: Repository introduction
uses: lowlighter/metrics@latest
with:
  filename: metrics.plugin.introduction.repository.svg
  token: ${{ secrets.METRICS_TOKEN }}
  template: repository
  repo: metrics
  base: header
  plugin_introduction: yes

```
<!--/examples-->


<!--header-->
<table>
  <tr><td colspan="2"><a href="/README.md#-plugins">← Back to plugins index</a></td></tr>
  <tr><th colspan="2"><h3>🏆 Achievements</h3></th></tr>
  <tr><td colspan="2" align="center"><p>This plugin displays several highlights about what an account has achieved on GitHub.</p>
</td></tr>
  <tr><th>⚠️ Disclaimer</th><td><p>This plugin is not affiliated, associated, authorized, endorsed by, or in any way officially connected with <a href="https://github.com">GitHub</a>.
All product and company names are trademarks™ or registered® trademarks of their respective holders.</p>
</td></tr>
  <tr>
    <th rowspan="3">Supported features<br><sub><a href="metadata.yml">→ Full specification</a></sub></th>
    <td><a href="/source/templates/classic/README.md"><code>📗 Classic template</code></a></td>
  </tr>
  <tr>
    <td><code>👤 Users</code> <code>👥 Organizations</code></td>
  </tr>
  <tr>
    <td><code>🔑 (scopeless)</code> <code>read:org (optional)</code> <code>read:user (optional)</code> <code>read:packages (optional)</code> <code>repo (optional)</code></td>
  </tr>
  <tr>
    <td colspan="2" align="center">
      <details open><summary>Compact display</summary><img src="https://github.com/lowlighter/metrics/blob/examples/metrics.plugin.achievements.compact.svg" alt=""></img></details>
      <details><summary>Detailed display</summary><img src="https://github.com/lowlighter/metrics/blob/examples/metrics.plugin.achievements.svg" alt=""></img></details>
      <img width="900" height="1" alt="">
    </td>
  </tr>
</table>
<!--/header-->

## ➡️ Available options

<!--options-->
<table>
  <tr>
    <td align="center" nowrap="nowrap">Option</i></td><td align="center" nowrap="nowrap">Description</td>
  </tr>
  <tr>
    <td nowrap="nowrap"><h4><code>plugin_achievements</code></h4></td>
    <td rowspan="2"><p>Enable achievements plugin</p>
<img width="900" height="1" alt=""></td>
  </tr>
  <tr>
    <td nowrap="nowrap">🌐 Web instances must configure <code>settings.json</code>:
<ul>
<li><i>metrics.run.puppeteer.scrapping</i></li>
</ul>
<b>type:</b> <code>boolean</code>
<br>
<b>default:</b> no<br></td>
  </tr>
  <tr>
    <td nowrap="nowrap"><h4><code>plugin_achievements_threshold</code></h4></td>
    <td rowspan="2"><p>Rank threshold filter</p>
<p>Use <code>X</code> to display achievements not yet unlocked</p>
<img width="900" height="1" alt=""></td>
  </tr>
  <tr>
    <td nowrap="nowrap"><b>type:</b> <code>string</code>
<br>
<b>default:</b> C<br>
<b>allowed values:</b><ul><li>S</li><li>A</li><li>B</li><li>C</li><li>X</li></ul></td>
  </tr>
  <tr>
    <td nowrap="nowrap"><h4><code>plugin_achievements_secrets</code></h4></td>
    <td rowspan="2"><p>Secrets achievements</p>
<img width="900" height="1" alt=""></td>
  </tr>
  <tr>
    <td nowrap="nowrap"><b>type:</b> <code>boolean</code>
<br>
<b>default:</b> yes<br></td>
  </tr>
  <tr>
    <td nowrap="nowrap"><h4><code>plugin_achievements_display</code></h4></td>
    <td rowspan="2"><p>Display style</p>
<ul>
<li><code>detailed</code>: display icon, name, description and ranking</li>
<li><code>compact</code>: display icon, name and value</li>
</ul>
<img width="900" height="1" alt=""></td>
  </tr>
  <tr>
    <td nowrap="nowrap"><b>type:</b> <code>string</code>
<br>
<b>default:</b> detailed<br>
<b>allowed values:</b><ul><li>detailed</li><li>compact</li></ul></td>
  </tr>
  <tr>
    <td nowrap="nowrap"><h4><code>plugin_achievements_limit</code></h4></td>
    <td rowspan="2"><p>Display limit</p>
<img width="900" height="1" alt=""></td>
  </tr>
  <tr>
    <td nowrap="nowrap"><b>type:</b> <code>number</code>
<i>(0 ≤
𝑥)</i>
<br>
<b>zero behaviour:</b> disable</br>
<b>default:</b> 0<br></td>
  </tr>
  <tr>
    <td nowrap="nowrap"><h4><code>plugin_achievements_ignored</code></h4></td>
    <td rowspan="2"><p>Ignored achievements</p>
<p>Use achievements names without their rank adjective (i.e. without &quot;great&quot;, &quot;super&quot; or &quot;master&quot;)</p>
<img width="900" height="1" alt=""></td>
  </tr>
  <tr>
    <td nowrap="nowrap"><b>type:</b> <code>array</code>
<i>(comma-separated)</i>
<br></td>
  </tr>
  <tr>
    <td nowrap="nowrap"><h4><code>plugin_achievements_only</code></h4></td>
    <td rowspan="2"><p>Showcased achievements</p>
<p>Use achievements names without their rank adjective (i.e. without &quot;great&quot;, &quot;super&quot; or &quot;master&quot;)</p>
<p>This option is equivalent to <a href="/source/plugins/achievements/README.md#plugin_achievements_ignored"><code>plugin_achievements_ignored</code></a> with all existing achievements except the ones listed in this option</p>
<img width="900" height="1" alt=""></td>
  </tr>
  <tr>
    <td nowrap="nowrap"><b>type:</b> <code>array</code>
<i>(comma-separated)</i>
<br></td>
  </tr>
</table>
<!--/options-->

## ℹ️ Examples workflows

<!--examples-->
```yaml
name: Detailed display
uses: lowlighter/metrics@latest
with:
  filename: metrics.plugin.achievements.svg
  token: ${{ secrets.METRICS_TOKEN }}
  base: ""
  plugin_achievements: yes
  plugin_achievements_only: sponsor, maintainer, octonaut

```
```yaml
name: Compact display
uses: lowlighter/metrics@latest
with:
  filename: metrics.plugin.achievements.compact.svg
  token: ${{ secrets.METRICS_TOKEN }}
  base: ""
  plugin_achievements: yes
  plugin_achievements_only: >-
    polyglot, stargazer, sponsor, deployer, member, maintainer, developer,
    scripter, packager, explorer, infographile, manager
  plugin_achievements_display: compact
  plugin_achievements_threshold: X

```
<!--/examples-->

<!--header-->
<table>
  <tr><td colspan="2"><a href="/README.md#-plugins">← Back to plugins index</a></td></tr>
  <tr><th colspan="2"><h3>🎭 Comment reactions</h3></th></tr>
  <tr><td colspan="2" align="center"><p>This plugin displays overall user reactions on recent issues, comments and discussions.</p>
</td></tr>
  <tr><th>⚠️ Disclaimer</th><td><p>This plugin is not affiliated, associated, authorized, endorsed by, or in any way officially connected with <a href="https://github.com">GitHub</a>.
All product and company names are trademarks™ or registered® trademarks of their respective holders.</p>
</td></tr>
  <tr>
    <th rowspan="3">Supported features<br><sub><a href="metadata.yml">→ Full specification</a></sub></th>
    <td><a href="/source/templates/classic/README.md"><code>📗 Classic template</code></a></td>
  </tr>
  <tr>
    <td><code>👤 Users</code></td>
  </tr>
  <tr>
    <td><code>🔑 (scopeless)</code> <code>read:org (optional)</code> <code>read:user (optional)</code> <code>read:packages (optional)</code> <code>repo (optional)</code></td>
  </tr>
  <tr>
    <td colspan="2" align="center">
      <img src="https://github.com/lowlighter/metrics/blob/examples/metrics.plugin.reactions.svg" alt=""></img>
      <img width="900" height="1" alt="">
    </td>
  </tr>
</table>
<!--/header-->

## ➡️ Available options

<!--options-->
<table>
  <tr>
    <td align="center" nowrap="nowrap">Option</i></td><td align="center" nowrap="nowrap">Description</td>
  </tr>
  <tr>
    <td nowrap="nowrap"><h4><code>plugin_reactions</code></h4></td>
    <td rowspan="2"><p>Enable reactions plugin</p>
<img width="900" height="1" alt=""></td>
  </tr>
  <tr>
    <td nowrap="nowrap"><b>type:</b> <code>boolean</code>
<br>
<b>default:</b> no<br></td>
  </tr>
  <tr>
    <td nowrap="nowrap"><h4><code>plugin_reactions_limit</code></h4></td>
    <td rowspan="2"><p>Display limit (issues and pull requests comments)</p>
<img width="900" height="1" alt=""></td>
  </tr>
  <tr>
    <td nowrap="nowrap"><b>type:</b> <code>number</code>
<i>(0 ≤
𝑥
≤ 1000)</i>
<br>
<b>default:</b> 200<br></td>
  </tr>
  <tr>
    <td nowrap="nowrap"><h4><code>plugin_reactions_limit_issues</code></h4></td>
    <td rowspan="2"><p>Display limit (issues and pull requests, first comment)</p>
<img width="900" height="1" alt=""></td>
  </tr>
  <tr>
    <td nowrap="nowrap"><b>type:</b> <code>number</code>
<i>(0 ≤
𝑥
≤ 1000)</i>
<br>
<b>default:</b> 100<br></td>
  </tr>
  <tr>
    <td nowrap="nowrap"><h4><code>plugin_reactions_limit_discussions</code></h4></td>
    <td rowspan="2"><p>Display limit (discussions, first comment)</p>
<img width="900" height="1" alt=""></td>
  </tr>
  <tr>
    <td nowrap="nowrap"><b>type:</b> <code>number</code>
<i>(0 ≤
𝑥
≤ 1000)</i>
<br>
<b>default:</b> 100<br></td>
  </tr>
  <tr>
    <td nowrap="nowrap"><h4><code>plugin_reactions_limit_discussions_comments</code></h4></td>
    <td rowspan="2"><p>Display limit (discussions comments)</p>
<img width="900" height="1" alt=""></td>
  </tr>
  <tr>
    <td nowrap="nowrap"><b>type:</b> <code>number</code>
<i>(0 ≤
𝑥
≤ 1000)</i>
<br>
<b>default:</b> 100<br></td>
  </tr>
  <tr>
    <td nowrap="nowrap"><h4><code>plugin_reactions_days</code></h4></td>
    <td rowspan="2"><p>Comments maximum age</p>
<img width="900" height="1" alt=""></td>
  </tr>
  <tr>
    <td nowrap="nowrap"><b>type:</b> <code>number</code>
<i>(0 ≤
𝑥)</i>
<br>
<b>zero behaviour:</b> disable</br>
<b>default:</b> 0<br></td>
  </tr>
  <tr>
    <td nowrap="nowrap"><h4><code>plugin_reactions_display</code></h4></td>
    <td rowspan="2"><p>Display mode</p>
<ul>
<li><code>absolute</code>: scale percentages using total reactions count</li>
<li><code>relative</code>: scale percentages using highest reaction count</li>
</ul>
<img width="900" height="1" alt=""></td>
  </tr>
  <tr>
    <td nowrap="nowrap"><b>type:</b> <code>string</code>
<br>
<b>default:</b> absolute<br>
<b>allowed values:</b><ul><li>absolute</li><li>relative</li></ul></td>
  </tr>
  <tr>
    <td nowrap="nowrap"><h4><code>plugin_reactions_details</code></h4></td>
    <td rowspan="2"><p>Additional details</p>
<img width="900" height="1" alt=""></td>
  </tr>
  <tr>
    <td nowrap="nowrap"><b>type:</b> <code>array</code>
<i>(comma-separated)</i>
<br>
<b>allowed values:</b><ul><li>count</li><li>percentage</li></ul></td>
  </tr>
  <tr>
    <td nowrap="nowrap"><h4><code>plugin_reactions_ignored</code></h4></td>
    <td rowspan="2"><p>Ignored users</p>
<p>Can be used to ignore bots activity</p>
<img width="900" height="1" alt=""></td>
  </tr>
  <tr>
    <td nowrap="nowrap">⏩ Inherits <code>users_ignored</code><br>
<b>type:</b> <code>array</code>
<i>(comma-separated)</i>
<br></td>
  </tr>
</table>
<!--/options-->

## ℹ️ Examples workflows

<!--examples-->
```yaml
name: Comment reactions
uses: lowlighter/metrics@latest
with:
  filename: metrics.plugin.reactions.svg
  token: ${{ secrets.METRICS_TOKEN }}
  base: ""
  plugin_reactions: yes
  plugin_reactions_limit: 100
  plugin_reactions_details: percentage

```
<!--/examples-->

<!--header-->
<table>
  <tr><td colspan="2"><a href="/README.md#-plugins">← Back to plugins index</a></td></tr>
  <tr><th colspan="2"><h3>🎟️ Follow-up of issues and pull requests</h3></th></tr>
  <tr><td colspan="2" align="center"><p>This plugin displays the ratio of open/closed issues and the ratio of open/merged pull requests across repositories.</p>
</td></tr>
  <tr><th>⚠️ Disclaimer</th><td><p>This plugin is not affiliated, associated, authorized, endorsed by, or in any way officially connected with <a href="https://github.com">GitHub</a>.
All product and company names are trademarks™ or registered® trademarks of their respective holders.</p>
</td></tr>
  <tr>
    <th rowspan="3">Supported features<br><sub><a href="metadata.yml">→ Full specification</a></sub></th>
    <td><a href="/source/templates/classic/README.md"><code>📗 Classic template</code></a> <a href="/source/templates/repository/README.md"><code>📘 Repository template</code></a></td>
  </tr>
  <tr>
    <td><code>👤 Users</code> <code>👥 Organizations</code> <code>📓 Repositories</code></td>
  </tr>
  <tr>
    <td><code>🔑 (scopeless)</code> <code>read:org (optional)</code> <code>read:user (optional)</code> <code>read:packages (optional)</code> <code>repo (optional)</code></td>
  </tr>
  <tr>
    <td colspan="2" align="center">
      <details open><summary>Indepth analysis</summary><img src="https://github.com/lowlighter/metrics/blob/examples/metrics.plugin.followup.indepth.svg" alt=""></img></details>
      <details><summary>Created on a user's repositories</summary><img src="https://github.com/lowlighter/metrics/blob/examples/metrics.plugin.followup.svg" alt=""></img></details>
      <details><summary>Created by a user</summary><img src="https://github.com/lowlighter/metrics/blob/examples/metrics.plugin.followup.user.svg" alt=""></img></details>
      <img width="900" height="1" alt="">
    </td>
  </tr>
</table>
<!--/header-->

## ➡️ Available options

<!--options-->
<table>
  <tr>
    <td align="center" nowrap="nowrap">Option</i></td><td align="center" nowrap="nowrap">Description</td>
  </tr>
  <tr>
    <td nowrap="nowrap"><h4><code>plugin_followup</code></h4></td>
    <td rowspan="2"><p>Enable followup plugin</p>
<img width="900" height="1" alt=""></td>
  </tr>
  <tr>
    <td nowrap="nowrap"><b>type:</b> <code>boolean</code>
<br>
<b>default:</b> no<br></td>
  </tr>
  <tr>
    <td nowrap="nowrap"><h4><code>plugin_followup_sections</code></h4></td>
    <td rowspan="2"><p>Displayed sections</p>
<ul>
<li><code>repositories</code>: overall status of issues and pull requests on your repositories</li>
<li><code>user</code>: overall status of issues and pull requests you have created on GitHub</li>
</ul>
<img width="900" height="1" alt=""></td>
  </tr>
  <tr>
    <td nowrap="nowrap"><b>type:</b> <code>array</code>
<i>(comma-separated)</i>
<br>
<b>default:</b> repositories<br>
<b>allowed values:</b><ul><li>repositories</li><li>user</li></ul></td>
  </tr>
  <tr>
    <td nowrap="nowrap"><h4><code>plugin_followup_indepth</code></h4></td>
    <td rowspan="2"><p>Indepth analysis</p>
<img width="900" height="1" alt=""></td>
  </tr>
  <tr>
    <td nowrap="nowrap">🌐 Web instances must configure <code>settings.json</code>:
<ul>
<li><i>metrics.api.github.overuse</i></li>
</ul>
<b>type:</b> <code>boolean</code>
<br>
<b>default:</b> no<br></td>
  </tr>
  <tr>
    <td nowrap="nowrap"><h4><code>plugin_followup_archived</code></h4></td>
    <td rowspan="2"><p>Include archived repositories</p>
<img width="900" height="1" alt=""></td>
  </tr>
  <tr>
    <td nowrap="nowrap"><b>type:</b> <code>boolean</code>
<br>
<b>default:</b> yes<br></td>
  </tr>
</table>
<!--/options-->

## 🔎 `indepth` mode

The `plugin_followup_indepth` option collects additional stats to differentiate issues and pull requests opened by maintainers and users.

It helps knowing whether repositories are also maintained by other users and give an overall health status of repositories.

> ⚠️ This mode will try to list users with push access to know who are the maintainers in order to place issues in the correct category, which requires a `repo` scope. If not available, it will consider that only the owner is a maintainer.

## ℹ️ Examples workflows

<!--examples-->
```yaml
name: Opened on user's repositories
uses: lowlighter/metrics@latest
with:
  filename: metrics.plugin.followup.svg
  token: ${{ secrets.METRICS_TOKEN }}
  base: ""
  plugin_followup: yes

```
```yaml
name: Opened by user
uses: lowlighter/metrics@latest
with:
  filename: metrics.plugin.followup.user.svg
  token: ${{ secrets.METRICS_TOKEN }}
  base: ""
  plugin_followup: yes
  plugin_followup_sections: user

```
```yaml
name: Indepth analysis
uses: lowlighter/metrics@latest
with:
  filename: metrics.plugin.followup.indepth.svg
  token: ${{ secrets.METRICS_TOKEN }}
  base: ""
  plugin_followup: yes
  plugin_followup_indepth: yes

```
```yaml
name: Exclude Archived
uses: lowlighter/metrics@latest
with:
  filename: metrics.plugin.followup.archived.svg
  token: ${{ secrets.METRICS_TOKEN }}
  base: ""
  plugin_followup: yes
  plugin_followup_archived: no

```
<!--/examples-->

<!--header-->
<table>
  <tr><td colspan="2"><a href="/README.md#-plugins">← Back to plugins index</a></td></tr>
  <tr><th colspan="2"><h3>💡 Coding habits and activity</h3></th></tr>
  <tr><td colspan="2" align="center"><p>This plugin displays coding habits based on recent activity, such as active hours and languages recently used.</p>
</td></tr>
  <tr><th>⚠️ Disclaimer</th><td><p>This plugin is not affiliated, associated, authorized, endorsed by, or in any way officially connected with <a href="https://github.com">GitHub</a>.
All product and company names are trademarks™ or registered® trademarks of their respective holders.</p>
</td></tr>
  <tr>
    <th rowspan="3">Supported features<br><sub><a href="metadata.yml">→ Full specification</a></sub></th>
    <td><a href="/source/templates/classic/README.md"><code>📗 Classic template</code></a></td>
  </tr>
  <tr>
    <td><code>👤 Users</code> <code>👥 Organizations</code></td>
  </tr>
  <tr>
    <td><code>🔑 (scopeless)</code> <code>read:org (optional)</code> <code>read:user (optional)</code> <code>read:packages (optional)</code> <code>repo (optional)</code></td>
  </tr>
  <tr>
    <td colspan="2" align="center">
      <details open><summary>Recent activity charts</summary><img src="https://github.com/lowlighter/metrics/blob/examples/metrics.plugin.habits.charts.svg" alt=""></img></details>
      <details open><summary>Mildly interesting facts</summary><img src="https://github.com/lowlighter/metrics/blob/examples/metrics.plugin.habits.facts.svg" alt=""></img></details>
      <img width="900" height="1" alt="">
    </td>
  </tr>
</table>
<!--/header-->

## ➡️ Available options

<!--options-->
<table>
  <tr>
    <td align="center" nowrap="nowrap">Option</i></td><td align="center" nowrap="nowrap">Description</td>
  </tr>
  <tr>
    <td nowrap="nowrap"><h4><code>plugin_habits</code></h4></td>
    <td rowspan="2"><p>Enable habits plugin</p>
<img width="900" height="1" alt=""></td>
  </tr>
  <tr>
    <td nowrap="nowrap"><b>type:</b> <code>boolean</code>
<br>
<b>default:</b> no<br></td>
  </tr>
  <tr>
    <td nowrap="nowrap"><h4><code>plugin_habits_from</code></h4></td>
    <td rowspan="2"><p>Events to use</p>
<p>A higher number will increase stats accuracy</p>
<img width="900" height="1" alt=""></td>
  </tr>
  <tr>
    <td nowrap="nowrap"><b>type:</b> <code>number</code>
<i>(1 ≤
𝑥
≤ 1000)</i>
<br>
<b>default:</b> 200<br></td>
  </tr>
  <tr>
    <td nowrap="nowrap"><h4><code>plugin_habits_skipped</code></h4></td>
    <td rowspan="2"><p>Skipped repositories</p>
<img width="900" height="1" alt=""></td>
  </tr>
  <tr>
    <td nowrap="nowrap">⏩ Inherits <code>repositories_skipped</code><br>
<b>type:</b> <code>array</code>
<i>(newline-separated)</i>
<br></td>
  </tr>
  <tr>
    <td nowrap="nowrap"><h4><code>plugin_habits_days</code></h4></td>
    <td rowspan="2"><p>Event maximum age</p>
<img width="900" height="1" alt=""></td>
  </tr>
  <tr>
    <td nowrap="nowrap"><b>type:</b> <code>number</code>
<i>(1 ≤
𝑥
≤ 30)</i>
<br>
<b>default:</b> 14<br></td>
  </tr>
  <tr>
    <td nowrap="nowrap"><h4><code>plugin_habits_facts</code></h4></td>
    <td rowspan="2"><p>Mildly interesting facts</p>
<p>It includes indentation type, average number of characters per line of code, and most active time and day</p>
<img width="900" height="1" alt=""></td>
  </tr>
  <tr>
    <td nowrap="nowrap"><b>type:</b> <code>boolean</code>
<br>
<b>default:</b> yes<br></td>
  </tr>
  <tr>
    <td nowrap="nowrap"><h4><code>plugin_habits_charts</code></h4></td>
    <td rowspan="2"><p>Charts</p>
<p>It includes commit activity per hour of day and commit activity per day of week
Recent language activity may also displayed (it requires extras features to be enabled for web instances) for historical reasons</p>
<img width="900" height="1" alt=""></td>
  </tr>
  <tr>
    <td nowrap="nowrap">🌐 Web instances must configure <code>settings.json</code>:
<ul>
<li><i>metrics.api.github.overuse</i></li>
<li><i>metrics.run.tempdir</i></li>
<li><i>metrics.run.git</i></li>
</ul>
<b>type:</b> <code>boolean</code>
<br>
<b>default:</b> no<br></td>
  </tr>
  <tr>
    <td nowrap="nowrap"><h4><code>plugin_habits_charts_type</code></h4></td>
    <td rowspan="2"><p>Charts display type</p>
<ul>
<li><code>classic</code>: <code>&lt;div&gt;</code> based charts, simple and lightweight</li>
<li><code>graph</code>: <code>&lt;svg&gt;</code> based charts, smooth</li>
</ul>
<blockquote>
<p>⚠️ <code>chartist</code> option has been deprecated and is now equivalent to <code>graph</code></p>
</blockquote>
<img width="900" height="1" alt=""></td>
  </tr>
  <tr>
    <td nowrap="nowrap">🌐 Web instances must configure <code>settings.json</code>:
<ul>
<li><i>metrics.npm.optional.d3</i></li>
</ul>
<b>type:</b> <code>string</code>
<br>
<b>default:</b> classic<br>
<b>allowed values:</b><ul><li>classic</li><li>graph</li><li>chartist</li></ul></td>
  </tr>
  <tr>
    <td nowrap="nowrap"><h4><code>plugin_habits_trim</code></h4></td>
    <td rowspan="2"><p>Trim unused hours on charts</p>
<img width="900" height="1" alt=""></td>
  </tr>
  <tr>
    <td nowrap="nowrap"><b>type:</b> <code>boolean</code>
<br>
<b>default:</b> no<br></td>
  </tr>
  <tr>
    <td nowrap="nowrap"><h4><code>plugin_habits_languages_limit</code></h4></td>
    <td rowspan="2"><p>Display limit (languages)</p>
<img width="900" height="1" alt=""></td>
  </tr>
  <tr>
    <td nowrap="nowrap"><b>type:</b> <code>number</code>
<i>(0 ≤
𝑥
≤ 8)</i>
<br>
<b>zero behaviour:</b> disable</br>
<b>default:</b> 8<br></td>
  </tr>
  <tr>
    <td nowrap="nowrap"><h4><code>plugin_habits_languages_threshold</code></h4></td>
    <td rowspan="2"><p>Display threshold (percentage)</p>
<img width="900" height="1" alt=""></td>
  </tr>
  <tr>
    <td nowrap="nowrap"><b>type:</b> <code>string</code>
<br>
<b>default:</b> 0%<br></td>
  </tr>
</table>
<!--/options-->

## 🌐 Configure used timezone

By default, dates use Greenwich meridian (GMT/UTC).

Configure `config_timezone` (see [supported timezone](https://en.wikipedia.org/wiki/List_of_tz_database_time_zones)) to avoid time offsets.

*Example: configuring timezone*
```yaml
- uses: lowlighter/metrics@latest
  with:
    config_timezone: Europe/Paris
```

## ℹ️ Examples workflows

<!--examples-->
```yaml
name: Mildly interesting facts
uses: lowlighter/metrics@latest
with:
  filename: metrics.plugin.habits.facts.svg
  token: ${{ secrets.METRICS_TOKEN }}
  base: ""
  plugin_habits: yes
  plugin_habits_facts: yes
  plugin_habits_charts: no
  config_timezone: Europe/Paris

```
```yaml
name: Recent activity charts
uses: lowlighter/metrics@latest
with:
  filename: metrics.plugin.habits.charts.svg
  token: ${{ secrets.METRICS_TOKEN }}
  base: ""
  plugin_habits: yes
  plugin_habits_facts: no
  plugin_habits_charts: yes
  config_timezone: Europe/Paris

```
<!--/examples-->

<!--header-->
<table>
  <tr><td colspan="2"><a href="/README.md#-plugins">← Back to plugins index</a></td></tr>
  <tr><th colspan="2"><h3>📜 Repository licenses</h3></th></tr>
  <tr><td colspan="2" align="center"><p>This plugin display repository license informations like permissions, limitations and conditions along with additional stats about dependencies.</p>
</td></tr>
  <tr><th>⚠️ Disclaimer</th><td><p>This plugin is not affiliated, associated, authorized, endorsed by, or in any way officially connected with <a href="https://github.com">GitHub</a>.
All product and company names are trademarks™ or registered® trademarks of their respective holders.</p>
</td></tr>
  <tr><th>ℹ Additional notes</th><td><blockquote>
<p>⚠️ This is <strong>NOT</strong> legal advice, use at your own risk</p>
</blockquote>
<blockquote>
<p>💣 This plugin <strong>SHOULD NOT</strong> be enabled on web instances, since it allows raw command injection.
This could result in compromised server!</p>
</blockquote>
</td></tr>
  <tr>
    <th rowspan="3">Supported features<br><sub><a href="metadata.yml">→ Full specification</a></sub></th>
    <td><a href="/source/templates/repository/README.md"><code>📘 Repository template</code></a></td>
  </tr>
  <tr>
    <td><code>📓 Repositories</code></td>
  </tr>
  <tr>
    <td><code>🔑 (scopeless)</code> <code>read:org (optional)</code> <code>read:user (optional)</code> <code>read:packages (optional)</code> <code>repo (optional)</code></td>
  </tr>
  <tr>
    <td colspan="2" align="center">
      <details open><summary>Permissions, limitations and conditions</summary><img src="https://github.com/lowlighter/metrics/blob/examples/metrics.plugin.licenses.svg" alt=""></img></details>
      <details open><summary>Licenses overview</summary><img src="https://github.com/lowlighter/metrics/blob/examples/metrics.plugin.licenses.ratio.svg" alt=""></img></details>
      <img width="900" height="1" alt="">
    </td>
  </tr>
</table>
<!--/header-->

## 🔎 Licenses analysis

Use to `plugin_licenses_setup` command to setup project dependencies.

*Example: setup a NodeJS project using `npm ci`*
```yml
- name: Licenses and permissions
  with:
    repo: metrics
    plugin_licenses: yes
    plugin_licenses_setup: npm ci
```

Dependencies will be analyzed by [GitHub licensed](https://github.com/github/licensed) and compared against GitHub known licenses.

> ⚠️ This is **NOT** legal advice, use at your own risk

> 💣 This plugin **SHOULD NOT** be enabled on web instances, since it allows raw command injection.
> This could result in compromised server!


## ➡️ Available options

<!--options-->
<table>
  <tr>
    <td align="center" nowrap="nowrap">Option</i></td><td align="center" nowrap="nowrap">Description</td>
  </tr>
  <tr>
    <td nowrap="nowrap"><h4><code>plugin_licenses</code></h4></td>
    <td rowspan="2"><p>Enable licenses plugin</p>
<img width="900" height="1" alt=""></td>
  </tr>
  <tr>
    <td nowrap="nowrap">🌐 Web instances must configure <code>settings.json</code>:
<ul>
<li><i>metrics.cpu.overuse</i></li>
<li><i>metrics.run.tempdir</i></li>
<li><i>metrics.run.git</i></li>
<li><i>metrics.run.licensed</i></li>
<li><i>metrics.run.user.cmd</i></li>
</ul>
<b>type:</b> <code>boolean</code>
<br>
<b>default:</b> no<br></td>
  </tr>
  <tr>
    <td nowrap="nowrap"><h4><code>plugin_licenses_setup</code></h4></td>
    <td rowspan="2"><p>Setup command</p>
<blockquote>
<p>ℹ️ Depending on the project, this may not be required.
The example command is intended for NodeJs projects that use <code>npm</code> to install their dependencies.</p>
</blockquote>
<img width="900" height="1" alt=""></td>
  </tr>
  <tr>
    <td nowrap="nowrap"><b>type:</b> <code>string</code>
<br></td>
  </tr>
  <tr>
    <td nowrap="nowrap"><h4><code>plugin_licenses_ratio</code></h4></td>
    <td rowspan="2"><p>Used licenses ratio</p>
<img width="900" height="1" alt=""></td>
  </tr>
  <tr>
    <td nowrap="nowrap"><b>type:</b> <code>boolean</code>
<br>
<b>default:</b> no<br></td>
  </tr>
  <tr>
    <td nowrap="nowrap"><h4><code>plugin_licenses_legal</code></h4></td>
    <td rowspan="2"><p>Permissions, limitations and conditions about used licenses</p>
<img width="900" height="1" alt=""></td>
  </tr>
  <tr>
    <td nowrap="nowrap"><b>type:</b> <code>boolean</code>
<br>
<b>default:</b> yes<br></td>
  </tr>
</table>
<!--/options-->

## ℹ️ Examples workflows

<!--examples-->
```yaml
name: Licenses and permissions
with:
  filename: metrics.plugin.licenses.svg
  token: ${{ secrets.METRICS_TOKEN }}
  base: ""
  template: repository
  repo: metrics
  plugin_licenses: yes
  plugin_licenses_setup: bash -c '[[ -f package.json ]] && npm ci || true'

```
```yaml
name: Licenses with open-source ratio graphs
uses: lowlighter/metrics@latest
with:
  filename: metrics.plugin.licenses.ratio.svg
  token: ${{ secrets.METRICS_TOKEN }}
  base: ""
  template: repository
  repo: metrics
  plugin_licenses: yes
  plugin_licenses_setup: bash -c '[[ -f package.json ]] && npm ci || true'
  plugin_licenses_legal: no
  plugin_licenses_ratio: yes

```
<!--/examples-->

<!--header-->
<table>
  <tr><td colspan="2"><a href="/README.md#-plugins">← Back to plugins index</a></td></tr>
  <tr><th colspan="2"><h3>📌 Starred topics</h3></th></tr>
  <tr><td colspan="2" align="center"><p>This plugin displays <a href="https://github.com/stars?filter=topics">starred topics</a>.</p>
<p>Check out <a href="https://github.com/topics">GitHub topics</a> to search interesting topics.</p>
</td></tr>
  <tr><th>⚠️ Disclaimer</th><td><p>This plugin is not affiliated, associated, authorized, endorsed by, or in any way officially connected with <a href="https://github.com">GitHub</a>.
All product and company names are trademarks™ or registered® trademarks of their respective holders.</p>
</td></tr>
  <tr>
    <th rowspan="3">Supported features<br><sub><a href="metadata.yml">→ Full specification</a></sub></th>
    <td><a href="/source/templates/classic/README.md"><code>📗 Classic template</code></a> <a href="/source/templates/markdown/README.md"><code>📒 Markdown template</code></a></td>
  </tr>
  <tr>
    <td><code>👤 Users</code></td>
  </tr>
  <tr>
    <td><i>No tokens are required for this plugin</i></td>
  </tr>
  <tr>
    <td colspan="2" align="center">
      <details open><summary>With icons</summary><img src="https://github.com/lowlighter/metrics/blob/examples/metrics.plugin.topics.icons.svg" alt=""></img></details>
      <details open><summary>With labels</summary><img src="https://github.com/lowlighter/metrics/blob/examples/metrics.plugin.topics.svg" alt=""></img></details>
      <img width="900" height="1" alt="">
    </td>
  </tr>
</table>
<!--/header-->

## ➡️ Available options

<!--options-->
<table>
  <tr>
    <td align="center" nowrap="nowrap">Option</i></td><td align="center" nowrap="nowrap">Description</td>
  </tr>
  <tr>
    <td nowrap="nowrap"><h4><code>plugin_topics</code></h4></td>
    <td rowspan="2"><p>Enable topics plugin</p>
<img width="900" height="1" alt=""></td>
  </tr>
  <tr>
    <td nowrap="nowrap">🌐 Web instances must configure <code>settings.json</code>:
<ul>
<li><i>metrics.run.puppeteer.scrapping</i></li>
</ul>
<b>type:</b> <code>boolean</code>
<br>
<b>default:</b> no<br></td>
  </tr>
  <tr>
    <td nowrap="nowrap"><h4><code>plugin_topics_mode</code></h4></td>
    <td rowspan="2"><p>Display mode</p>
<ul>
<li><code>labels</code>: display labels</li>
<li><code>icons</code>: display icons <em>(topics without icons will not be displayed)</em></li>
<li><code>starred</code>: alias for <code>labels</code></li>
<li><code>mastered</code>: alias for <code>icons</code></li>
</ul>
<img width="900" height="1" alt=""></td>
  </tr>
  <tr>
    <td nowrap="nowrap"><b>type:</b> <code>string</code>
<br>
<b>default:</b> starred<br>
<b>allowed values:</b><ul><li>labels</li><li>icons</li><li>starred</li><li>mastered</li></ul></td>
  </tr>
  <tr>
    <td nowrap="nowrap"><h4><code>plugin_topics_sort</code></h4></td>
    <td rowspan="2"><p>Sorting method</p>
<ul>
<li><code>stars</code>: sort by most stars</li>
<li><code>activity</code>: sort by recent activity</li>
<li><code>starred</code>: sort by starred date</li>
<li><code>random</code>: sort randomly</li>
</ul>
<img width="900" height="1" alt=""></td>
  </tr>
  <tr>
    <td nowrap="nowrap"><b>type:</b> <code>string</code>
<br>
<b>default:</b> stars<br>
<b>allowed values:</b><ul><li>stars</li><li>activity</li><li>starred</li><li>random</li></ul></td>
  </tr>
  <tr>
    <td nowrap="nowrap"><h4><code>plugin_topics_limit</code></h4></td>
    <td rowspan="2"><p>Display limit</p>
<img width="900" height="1" alt=""></td>
  </tr>
  <tr>
    <td nowrap="nowrap"><b>type:</b> <code>number</code>
<i>(0 ≤
𝑥
≤ 20)</i>
<br>
<b>zero behaviour:</b> disable</br>
<b>default:</b> 15<br></td>
  </tr>
</table>
<!--/options-->

## ℹ️ Examples workflows

<!--examples-->
```yaml
name: Labels
uses: lowlighter/metrics@latest
with:
  filename: metrics.plugin.topics.svg
  token: NOT_NEEDED
  base: ""
  plugin_topics: yes
  plugin_topics_limit: 12

```
```yaml
name: Icons
uses: lowlighter/metrics@latest
with:
  filename: metrics.plugin.topics.icons.svg
  token: NOT_NEEDED
  base: ""
  plugin_topics: yes
  plugin_topics_limit: 0
  plugin_topics_mode: icons

```
<!--/examples-->

<!--header-->
<table>
  <tr><td colspan="2"><a href="/README.md#-plugins">← Back to plugins index</a></td></tr>
  <tr><th colspan="2"><h3>🈷️ Languages activity</h3></th></tr>
  <tr><td colspan="2" align="center"><p>This plugin can display which languages you use across all repositories you contributed to.</p>
</td></tr>
  <tr><th>⚠️ Disclaimer</th><td><p>This plugin is not affiliated, associated, authorized, endorsed by, or in any way officially connected with <a href="https://github.com">GitHub</a>.
All product and company names are trademarks™ or registered® trademarks of their respective holders.</p>
</td></tr>
  <tr>
    <th rowspan="3">Supported features<br><sub><a href="metadata.yml">→ Full specification</a></sub></th>
    <td><a href="/source/templates/classic/README.md"><code>📗 Classic template</code></a> <a href="/source/templates/repository/README.md"><code>📘 Repository template</code></a> <a href="/source/templates/terminal/README.md"><code>📙 Terminal template</code></a></td>
  </tr>
  <tr>
    <td><code>👤 Users</code> <code>👥 Organizations</code> <code>📓 Repositories</code></td>
  </tr>
  <tr>
    <td><code>🔑 (scopeless)</code> <code>read:org (optional)</code> <code>read:user (optional)</code> <code>read:packages (optional)</code> <code>repo (optional)</code></td>
  </tr>
  <tr>
    <td colspan="2" align="center">
      <details open><summary>Indepth analysis (clone and analyze repositories)</summary><img src="https://github.com/lowlighter/metrics/blob/examples/metrics.plugin.languages.indepth.svg" alt=""></img></details>
      <details open><summary>Recently used (analyze recent activity events)</summary><img src="https://github.com/lowlighter/metrics/blob/examples/metrics.plugin.languages.recent.svg" alt=""></img></details>
      <details><summary>Default algorithm</summary><img src="https://github.com/lowlighter/metrics/blob/examples/metrics.plugin.languages.svg" alt=""></img></details>
      <details><summary>Default algorithm (with details)</summary><img src="https://github.com/lowlighter/metrics/blob/examples/metrics.plugin.languages.details.svg" alt=""></img></details>
      <img width="900" height="1" alt="">
    </td>
  </tr>
</table>
<!--/header-->

## ➡️ Available options

<!--options-->
<table>
  <tr>
    <td align="center" nowrap="nowrap">Option</i></td><td align="center" nowrap="nowrap">Description</td>
  </tr>
  <tr>
    <td nowrap="nowrap"><h4><code>plugin_languages</code></h4></td>
    <td rowspan="2"><p>Enable languages plugin</p>
<img width="900" height="1" alt=""></td>
  </tr>
  <tr>
    <td nowrap="nowrap"><b>type:</b> <code>boolean</code>
<br>
<b>default:</b> no<br></td>
  </tr>
  <tr>
    <td nowrap="nowrap"><h4><code>plugin_languages_ignored</code></h4></td>
    <td rowspan="2"><p>Ignored languages</p>
<img width="900" height="1" alt=""></td>
  </tr>
  <tr>
    <td nowrap="nowrap"><b>type:</b> <code>array</code>
<i>(comma-separated)</i>
<br></td>
  </tr>
  <tr>
    <td nowrap="nowrap"><h4><code>plugin_languages_skipped</code></h4></td>
    <td rowspan="2"><p>Skipped repositories</p>
<img width="900" height="1" alt=""></td>
  </tr>
  <tr>
    <td nowrap="nowrap">⏩ Inherits <code>repositories_skipped</code><br>
<b>type:</b> <code>array</code>
<i>(newline-separated)</i>
<br></td>
  </tr>
  <tr>
    <td nowrap="nowrap"><h4><code>plugin_languages_limit</code></h4></td>
    <td rowspan="2"><p>Display limit</p>
<img width="900" height="1" alt=""></td>
  </tr>
  <tr>
    <td nowrap="nowrap"><b>type:</b> <code>number</code>
<i>(0 ≤
𝑥
≤ 8)</i>
<br>
<b>zero behaviour:</b> disable</br>
<b>default:</b> 8<br></td>
  </tr>
  <tr>
    <td nowrap="nowrap"><h4><code>plugin_languages_threshold</code></h4></td>
    <td rowspan="2"><p>Display threshold (percentage)</p>
<img width="900" height="1" alt=""></td>
  </tr>
  <tr>
    <td nowrap="nowrap"><b>type:</b> <code>string</code>
<br>
<b>default:</b> 0%<br></td>
  </tr>
  <tr>
    <td nowrap="nowrap"><h4><code>plugin_languages_other</code></h4></td>
    <td rowspan="2"><p>Group unknown, ignored and over-limit languages into &quot;Other&quot; category</p>
<p>If this option is enabled, &quot;Other&quot; category will not be subject to <a href="/source/plugins/languages/README.md#plugin_languages_threshold"><code>plugin_languages_threshold</code></a>.
It will be automatically hidden if empty.</p>
<img width="900" height="1" alt=""></td>
  </tr>
  <tr>
    <td nowrap="nowrap"><b>type:</b> <code>boolean</code>
<br>
<b>default:</b> no<br></td>
  </tr>
  <tr>
    <td nowrap="nowrap"><h4><code>plugin_languages_colors</code></h4></td>
    <td rowspan="2"><p>Custom languages colors</p>
<img width="900" height="1" alt=""></td>
  </tr>
  <tr>
    <td nowrap="nowrap"><b>type:</b> <code>array</code>
<i>(comma-separated)</i>
<br>
<b>default:</b> github<br></td>
  </tr>
  <tr>
    <td nowrap="nowrap"><h4><code>plugin_languages_aliases</code></h4></td>
    <td rowspan="2"><p>Custom languages names</p>
<img width="900" height="1" alt=""></td>
  </tr>
  <tr>
    <td nowrap="nowrap"><b>type:</b> <code>string</code>
<br></td>
  </tr>
  <tr>
    <td nowrap="nowrap"><h4><code>plugin_languages_sections</code></h4></td>
    <td rowspan="2"><p>Displayed sections</p>
<p>Note that <code>recently-used</code> is only available when <a href="/source/plugins/languages/README.md#plugin_languages_indepth"><code>plugin_languages_indepth</code></a> is enabled</p>
<img width="900" height="1" alt=""></td>
  </tr>
  <tr>
    <td nowrap="nowrap"><b>type:</b> <code>array</code>
<i>(comma-separated)</i>
<br>
<b>default:</b> most-used<br>
<b>allowed values:</b><ul><li>most-used</li><li>recently-used</li></ul></td>
  </tr>
  <tr>
    <td nowrap="nowrap"><h4><code>plugin_languages_details</code></h4></td>
    <td rowspan="2"><p>Additional details</p>
<p>Note that <code>lines</code> is only available when <a href="/source/plugins/languages/README.md#plugin_languages_indepth"><code>plugin_languages_indepth</code></a> is enabled</p>
<img width="900" height="1" alt=""></td>
  </tr>
  <tr>
    <td nowrap="nowrap"><b>type:</b> <code>array</code>
<i>(comma-separated)</i>
<br>
<b>allowed values:</b><ul><li>bytes-size</li><li>percentage</li><li>lines</li></ul></td>
  </tr>
  <tr>
    <td nowrap="nowrap"><h4><code>plugin_languages_indepth</code></h4></td>
    <td rowspan="2"><p>Indepth mode</p>
<blockquote>
<p>⚠️ read documentation first</p>
</blockquote>
<img width="900" height="1" alt=""></td>
  </tr>
  <tr>
    <td nowrap="nowrap">🌐 Web instances must configure <code>settings.json</code>:
<ul>
<li><i>metrics.cpu.overuse</i></li>
<li><i>metrics.run.tempdir</i></li>
<li><i>metrics.run.git</i></li>
</ul>
<b>type:</b> <code>boolean</code>
<br>
<b>default:</b> false<br></td>
  </tr>
  <tr>
    <td nowrap="nowrap"><h4><code>plugin_languages_indepth_custom</code></h4></td>
    <td rowspan="2"><p>Indepth mode - Custom repositories</p>
<p>Specify a list of additional repositories to analyze.</p>
<p>Below are the supported syntax formats:</p>
<ul>
<li><code>owner/repo</code> (e.g. <code>lowlighter/metrics</code>)</li>
<li><code>owner/repo@branch</code> (e.g. <code>lowlighter/metrics@main</code>)</li>
<li><code>owner/repo@branch:commits</code> (e.g. <code>lowlighter/metrics@main:v1.0..v1.1</code>)<ul>
<li>See <a href="https://git-scm.com/docs/git-rev-list#_description"><code>git rev-list</code></a> documentation for more information about <code>commits</code> syntax</li>
</ul>
</li>
</ul>
<p>It is possible to specify repositories that are not hosted on <a href="https://github.com">github.com</a> by passing a full url instead.
In this case the repository must be accessible directly.</p>
<blockquote>
<p>ℹ️ This option bypass <a href="/source/plugins/languages/README.md#plugin_languages_skipped"><code>plugin_languages_skipped</code></a></p>
</blockquote>
<img width="900" height="1" alt=""></td>
  </tr>
  <tr>
    <td nowrap="nowrap"><b>type:</b> <code>array</code>
<i>(comma-separated)</i>
<br></td>
  </tr>
  <tr>
    <td nowrap="nowrap"><h4><code>plugin_languages_analysis_timeout</code></h4></td>
    <td rowspan="2"><p>Indepth mode - Analysis timeout</p>
<img width="900" height="1" alt=""></td>
  </tr>
  <tr>
    <td nowrap="nowrap"><b>type:</b> <code>number</code>
<i>(1 ≤
𝑥
≤ 60)</i>
<br>
<b>default:</b> 15<br></td>
  </tr>
  <tr>
    <td nowrap="nowrap"><h4><code>plugin_languages_analysis_timeout_repositories</code></h4></td>
    <td rowspan="2"><p>Indepth mode - Analysis timeout (repositories)</p>
<img width="900" height="1" alt=""></td>
  </tr>
  <tr>
    <td nowrap="nowrap"><b>type:</b> <code>number</code>
<i>(0 ≤
𝑥
≤ 15)</i>
<br>
<b>zero behaviour:</b> disable</br>
<b>default:</b> 7.5<br></td>
  </tr>
  <tr>
    <td nowrap="nowrap"><h4><code>plugin_languages_categories</code></h4></td>
    <td rowspan="2"><p>Indepth mode - Displayed categories (most-used section)</p>
<img width="900" height="1" alt=""></td>
  </tr>
  <tr>
    <td nowrap="nowrap"><b>type:</b> <code>array</code>
<i>(comma-separated)</i>
<br>
<b>default:</b> markup, programming<br>
<b>allowed values:</b><ul><li>data</li><li>markup</li><li>programming</li><li>prose</li></ul></td>
  </tr>
  <tr>
    <td nowrap="nowrap"><h4><code>plugin_languages_recent_categories</code></h4></td>
    <td rowspan="2"><p>Indepth mode - Displayed categories (recently-used section)</p>
<img width="900" height="1" alt=""></td>
  </tr>
  <tr>
    <td nowrap="nowrap"><b>type:</b> <code>array</code>
<i>(comma-separated)</i>
<br>
<b>default:</b> markup, programming<br>
<b>allowed values:</b><ul><li>data</li><li>markup</li><li>programming</li><li>prose</li></ul></td>
  </tr>
  <tr>
    <td nowrap="nowrap"><h4><code>plugin_languages_recent_load</code></h4></td>
    <td rowspan="2"><p>Indepth mode - Events to load (recently-used section)</p>
<img width="900" height="1" alt=""></td>
  </tr>
  <tr>
    <td nowrap="nowrap"><b>type:</b> <code>number</code>
<i>(100 ≤
𝑥
≤ 1000)</i>
<br>
<b>default:</b> 300<br></td>
  </tr>
  <tr>
    <td nowrap="nowrap"><h4><code>plugin_languages_recent_days</code></h4></td>
    <td rowspan="2"><p>Indepth mode - Events maximum age (day, recently-used section)</p>
<img width="900" height="1" alt=""></td>
  </tr>
  <tr>
    <td nowrap="nowrap"><b>type:</b> <code>number</code>
<i>(0 ≤
𝑥
≤ 365)</i>
<br>
<b>zero behaviour:</b> disable</br>
<b>default:</b> 14<br></td>
  </tr>
</table>
<!--/options-->

## 🔎 `indepth` mode

The default algorithm uses the top languages from each repository you contributed to using GitHub GraphQL API (which is similar to the displayed languages bar on github.com). When working in collaborative projects with a lot of people, these numbers may be less representative of your actual work.

The `plugin_languages_indepth` option lets you use a more advanced algorithm for more accurate statistics.
Under the hood, it will clone your repositories, run [linguist-js](https://github.com/Nixinova/Linguist) (a JavaScript port of [GitHub linguist](https://github.com/github/linguist)) and iterate over patches matching your `commits_authoring` setting.

Since git lets you use any email and username for commits, *metrics* may not be able to detect a commit ownership if it isn't the same as your GitHub personal data. By default, it will use your GitHub username, but you can configure additional matching usernames and email addresses using `commits_authoring` option.

*Example: configuring `indepth` mode*
```yml
- uses: lowlighter/metrics@latest
  with:
    plugin_languages: yes
    plugin_languages_indepth: yes
    commits_authoring: firstname lastname, username, username@users.noreply.github.com
```

> 💡 This feature unlocks the `lines` option in `plugin_languages_details`

> ⚠️ This feature significantly increase workflow time

> ⚠️ Since this mode iterates over **each matching commit of each repository**, it is not suited for large code base, especially those with a large amount of commits and the ones containing binaries. While `plugin_languages_analysis_timeout` and `plugin_languages_analysis_timeout_repositories` can be used to increase the default timeout for analysis, please be responsible and keep this feature disabled if it cannot work on your account to save GitHub resources and our planet 🌏

> ⚠️ Although *metrics* does not send any code to external sources, repositories are temporarily cloned on the GitHub Action runner. It is advised to keep this option disabled when working with sensitive data or company code. Use at your own risk, *metrics* and its authors **cannot** be held responsible for any resulting code leaks. Source code is available for auditing at [analyzers.mjs](/source/plugins/languages/analyzers.mjs).

> 🌐 Web instances must enable this feature in `settings.json`

Below is a summary of the process used to compute indepth statistics:

## Most used mode

1. Fetch GPG keys linked to your GitHub account
  - automatically add attached emails to `commits_authoring`
  - *web-flow* (GitHub's public key for changes made through web-ui) is also fetched
2. Import GPG keys so they can be used to verify commits later
3. Iterate through repositories
  - early break if `plugin_languages_analysis_timeout` is reached
  - skip repository if it matches `plugin_languages_skipped`
  - include repositories from `plugin_languages_indepth_custom`
    - a specific branch and commit range can be used
    - a source other than github.com can be used
4. Clone repository
  - target branch is checkout
5. List of authored commits is computed
  - using `git log --author` and `commits_authoring` to search in commit headers
  - using `git log --grep` and `commits_authoring` to search in commit body
  - ensure these are within the range specified by `plugin_languages_indepth_custom` (if applicable)
6. Process authored commits
  - early break if `plugin_languages_analysis_timeout_repositories` is reached
  - using `git verify-commit` to check authenticity against imported GPG keys
  - using `git log --patch` to extract added/deleted lines/bytes from each file
  - using [GitHub linguist](https://github.com/github/linguist) ([linguist-js](https://github.com/Nixinova/LinguistJS)) to detect language for each file
    - respect `plugin_languages_categories` option
    - if a file has since been deleted or moved, checkout on the last commit file was present and run linguist again
7. Aggregate results

## Recently used mode

1. Fetch push events linked to your account (or target repository)
  - matching `plugin_languages_recent_load` and `plugin_languages_recent_days` options
  - matching committer emails from `commits_authoring`
2. Process authored commits
  - using [GitHub linguist](https://github.com/github/linguist) ([linguist-js](https://github.com/Nixinova/LinguistJS)) to detect language for each file
    - respect `plugin_languages_recent_categories` option
    - directly pass file content rather than performing I/O and simulating a git repository
3. Aggregate results

## 📅 Recently used languages

This feature uses a similar algorithm as `indepth` mode, but uses patches from your events feed instead.
It will fetch a specified amount of recent push events and perform linguistic analysis on it.

> ⚠️ Note that *metrics* won't be able to use more events than GitHub API is able to provide

*Example: display recently used languages from 400 GitHub events from last 2 weeks*
```yml
- uses: lowlighter/metrics@latest
  with:
    plugin_languages: yes
    plugin_languages_sections: recently-used
    plugin_languages_recent_load: 400
    plugin_languages_recent_days: 14
```

> 🌐 Web instances must enable this feature in `settings.json`

## 🥽 Controling which languages are displayed

Several options lets you customize which languages should be displayed.
It is possible to ignore completely languages or those lower than a given threshold, skip repositories, and filter by language categories.

*Example: hide HTML and CSS languages, skip lowlighter/metrics repository*
```yml
- uses: lowlighter/metrics@latest
  with:
    plugin_languages: yes
    plugin_languages_ignored: html, css
    plugin_languages_skipped: lowlighter/metrics
```

*Example: hide languages with less than 2% usage*
```yml
- uses: lowlighter/metrics@latest
  with:
    plugin_languages: yes
    plugin_languages_threshold: 2%
```

> 💡 The threshold feature will automatically scale remaining languages so the total percentage is always 100%. However, other stats like bytes count and lines are not affected.

When using `indepth` mode, it is possible to hide languages per category.
Supported categories are `data`, `markup`, `programming` and `prose`.

*Example: hide data and prose languages from stats*
```yml
- uses: lowlighter/metrics@latest
  with:
    plugin_languages: yes
    plugin_languages_categories: data, prose
    plugin_languages_recent_categories: data, prose
```

## 🎨 Using custom colors

The plugin uses GitHub language colors, but it may be hard to distinguish them depending on which languages you use.
It is possible to use custom colors using `plugin_languages_colors` option.

The following syntaxes are supported:
- A predefined set from [colorsets.json](colorsets.json) *(support limited to 8 languages max)*
- `${language}:${color}` to change the color of a language *(case insensitive)*
- `${n}:${color}` to change the color of the n-th language

Both hexadecimal and [named color](https://developer.mozilla.org/en-US/docs/Web/CSS/color_value) are supported.

*Example: using a predefined color set*
```yml
- uses: lowlighter/metrics@latest
  with:
    plugin_languages: yes
    plugin_languages_colors: rainbow
    plugin_languages_limit: 8
```

*Example: setting JavaScript to red, the first language to blue and the second one to `#ff00aa`*
```yml
- uses: lowlighter/metrics@latest
  with:
    plugin_languages: yes
    plugin_languages_colors: javascript:red, 0:blue, 1:#ff00aa
```

## ✍️ Using custom languages name

This plugin is limited by [GitHub linguist](https://github.com/github/linguist) capabilities, meaning that some languages may be mislabeled in some cases.

To mitigate this, it is possible to use `plugin_languages_aliases` option and provide a list of overrides using the following syntax: `${language}:${alias}` *(case insensitive)*.

*Example: display JavaScript as JS and TypeScript as TS*
```yml
- uses: lowlighter/metrics@latest
  with:
    plugin_languages: yes
    plugin_languages_aliases: javascript:JS typescript:TS
```

## ℹ️ Examples workflows

<!--examples-->
```yaml
name: Most used
uses: lowlighter/metrics@latest
with:
  filename: metrics.plugin.languages.svg
  token: ${{ secrets.METRICS_TOKEN }}
  base: ""
  plugin_languages: yes
  plugin_languages_ignored: >-
    html, css, tex, less, dockerfile, makefile, qmake, lex, cmake, shell,
    gnuplot
  plugin_languages_limit: 4

```
```yaml
name: Most used (with details)
uses: lowlighter/metrics@latest
with:
  filename: metrics.plugin.languages.details.svg
  token: ${{ secrets.METRICS_TOKEN }}
  base: ""
  plugin_languages: yes
  plugin_languages_ignored: >-
    html, css, tex, less, dockerfile, makefile, qmake, lex, cmake, shell,
    gnuplot
  plugin_languages_details: bytes-size, percentage
  plugin_languages_limit: 4

```
```yaml
name: Recently used
uses: lowlighter/metrics@latest
with:
  filename: metrics.plugin.languages.recent.svg
  token: ${{ secrets.METRICS_TOKEN }}
  base: ""
  plugin_languages: yes
  plugin_languages_ignored: >-
    html, css, tex, less, dockerfile, makefile, qmake, lex, cmake, shell,
    gnuplot
  plugin_languages_sections: recently-used
  plugin_languages_details: bytes-size, percentage
  plugin_languages_limit: 4

```
```yaml
name: Indepth analysis
uses: lowlighter/metrics@latest
with:
  filename: metrics.plugin.languages.indepth.svg
  token: ${{ secrets.METRICS_TOKEN }}
  base: ""
  plugin_languages: yes
  plugin_languages_ignored: >-
    html, css, tex, less, dockerfile, makefile, qmake, lex, cmake, shell,
    gnuplot
  plugin_languages_indepth: yes
  plugin_languages_details: lines, bytes-size
  plugin_languages_limit: 4
  plugin_languages_analysis_timeout: 15

```
<!--/examples-->

<!--header-->
<table>
  <tr><td colspan="2"><a href="/README.md#-plugins">← Back to plugins index</a></td></tr>
  <tr><th colspan="2"><h3>✨ Stargazers</h3></th></tr>
  <tr><td colspan="2" align="center"><p>This plugin displays stargazers evolution across affiliated repositories.</p>
</td></tr>
  <tr><th>⚠️ Disclaimer</th><td><p>This plugin is not affiliated, associated, authorized, endorsed by, or in any way officially connected with <a href="https://github.com">GitHub</a>.
All product and company names are trademarks™ or registered® trademarks of their respective holders.</p>
</td></tr>
  <tr>
    <th rowspan="3">Supported features<br><sub><a href="metadata.yml">→ Full specification</a></sub></th>
    <td><a href="/source/templates/classic/README.md"><code>📗 Classic template</code></a> <a href="/source/templates/repository/README.md"><code>📘 Repository template</code></a></td>
  </tr>
  <tr>
    <td><code>👤 Users</code> <code>👥 Organizations</code> <code>📓 Repositories</code></td>
  </tr>
  <tr>
    <td><code>🔑 (scopeless)</code> <code>🗝️ plugin_stargazers_worldmap_token</code> <code>read:org (optional)</code> <code>read:user (optional)</code> <code>read:packages (optional)</code> <code>repo (optional)</code></td>
  </tr>
  <tr>
    <td colspan="2" align="center">
      <details open><summary>Classic charts</summary><img src="https://github.com/lowlighter/metrics/blob/examples/metrics.plugin.stargazers.svg" alt=""></img></details>
      <details><summary>Graph charts</summary><img src="https://github.com/lowlighter/metrics/blob/examples/metrics.plugin.stargazers.graph.svg" alt=""></img></details>
      <details open><summary>Worldmap</summary><img src="https://github.com/lowlighter/metrics/blob/examples/metrics.plugin.stargazers.worldmap.svg" alt=""></img></details>
      <img width="900" height="1" alt="">
    </td>
  </tr>
</table>
<!--/header-->

## 🗝️ Obtaining a Google Maps API token

Some features like `plugin_stagazers_worldmap` require a Google Geocoding API token.
Follow instructions from their [documentation](https://developers.google.com/maps/documentation/geocoding/get-api-key) for more informations.

> 💳 A billing account is required to get a token. However a recurring [monthly credit](https://developers.google.com/maps/billing-credits#monthly) is offered which means you should not be charged if you don't exceed the free quota.
>
> It is advised to set the quota limit at 1200 requests per day
>
> Use at your own risk, *metrics* and its authors cannot be held responsible for anything charged.

## ➡️ Available options

<!--options-->
<table>
  <tr>
    <td align="center" nowrap="nowrap">Option</i></td><td align="center" nowrap="nowrap">Description</td>
  </tr>
  <tr>
    <td nowrap="nowrap"><h4><code>plugin_stargazers</code></h4></td>
    <td rowspan="2"><p>Enable stargazers plugin</p>
<img width="900" height="1" alt=""></td>
  </tr>
  <tr>
    <td nowrap="nowrap"><b>type:</b> <code>boolean</code>
<br>
<b>default:</b> no<br></td>
  </tr>
  <tr>
    <td nowrap="nowrap"><h4><code>plugin_stargazers_days</code></h4></td>
    <td rowspan="2"><p>Time range</p>
<p>If set to <code>0</code> the account registration date will be used.</p>
<img width="900" height="1" alt=""></td>
  </tr>
  <tr>
    <td nowrap="nowrap"><b>type:</b> <code>number</code>
<i>(0 ≤
𝑥)</i>
<br>
<b>zero behaviour:</b> see description</br>
<b>default:</b> 14<br></td>
  </tr>
  <tr>
    <td nowrap="nowrap"><h4><code>plugin_stargazers_charts</code></h4></td>
    <td rowspan="2"><p>Charts</p>
<p>It includes total number of stargazers evolution, along with the number of new stars per day over the last two weeks.</p>
<img width="900" height="1" alt=""></td>
  </tr>
  <tr>
    <td nowrap="nowrap"><b>type:</b> <code>boolean</code>
<br>
<b>default:</b> yes<br></td>
  </tr>
  <tr>
    <td nowrap="nowrap"><h4><code>plugin_stargazers_charts_type</code></h4></td>
    <td rowspan="2"><p>Charts display type</p>
<ul>
<li><code>classic</code>: <code>&lt;div&gt;</code> based charts, simple and lightweight</li>
<li><code>graph</code>: <code>&lt;svg&gt;</code> based charts, smooth</li>
</ul>
<blockquote>
<p>⚠️ <code>chartist</code> option has been deprecated and is now equivalent to <code>graph</code></p>
</blockquote>
<img width="900" height="1" alt=""></td>
  </tr>
  <tr>
    <td nowrap="nowrap">🌐 Web instances must configure <code>settings.json</code>:
<ul>
<li><i>metrics.npm.optional.d3</i></li>
</ul>
<b>type:</b> <code>string</code>
<br>
<b>default:</b> classic<br>
<b>allowed values:</b><ul><li>classic</li><li>graph</li><li>chartist</li></ul></td>
  </tr>
  <tr>
    <td nowrap="nowrap"><h4><code>plugin_stargazers_worldmap</code></h4></td>
    <td rowspan="2"><p>Stargazers worldmap</p>
<img width="900" height="1" alt=""></td>
  </tr>
  <tr>
    <td nowrap="nowrap">🌐 Web instances must configure <code>settings.json</code>:
<ul>
<li><i>metrics.api.google.maps</i></li>
<li><i>metrics.npm.optional.d3</i></li>
</ul>
<b>type:</b> <code>boolean</code>
<br>
<b>default:</b> no<br></td>
  </tr>
  <tr>
    <td nowrap="nowrap"><h4><code>plugin_stargazers_worldmap_token</code></h4></td>
    <td rowspan="2"><p>Stargazers worldmap token</p>
<img width="900" height="1" alt=""></td>
  </tr>
  <tr>
    <td nowrap="nowrap">🔐 Token<br>
<b>type:</b> <code>token</code>
<br></td>
  </tr>
  <tr>
    <td nowrap="nowrap"><h4><code>plugin_stargazers_worldmap_sample</code></h4></td>
    <td rowspan="2"><p>Stargazers worldmap sample</p>
<p>Use this setting to randomly sample and limit your stargazers.
Helps to avoid consuming too much Google Geocoding API requests while still being representative.</p>
<img width="900" height="1" alt=""></td>
  </tr>
  <tr>
    <td nowrap="nowrap"><b>type:</b> <code>number</code>
<i>(0 ≤
𝑥)</i>
<br>
<b>zero behaviour:</b> disable</br>
<b>default:</b> 0<br></td>
  </tr>
</table>
<!--/options-->

## ℹ️ Examples workflows

<!--examples-->
```yaml
name: Using classic charts
uses: lowlighter/metrics@latest
with:
  filename: metrics.plugin.stargazers.svg
  token: ${{ secrets.METRICS_TOKEN }}
  base: ""
  plugin_stargazers: yes

```
```yaml
name: Using graph charts
uses: lowlighter/metrics@latest
with:
  filename: metrics.plugin.stargazers.graph.svg
  token: ${{ secrets.METRICS_TOKEN }}
  base: ""
  plugin_stargazers: yes
  plugin_stargazers_charts_type: graph

```
```yaml
name: With worldmap
uses: lowlighter/metrics@latest
with:
  filename: metrics.plugin.stargazers.worldmap.svg
  token: ${{ secrets.METRICS_TOKEN }}
  base: ""
  plugin_stargazers: yes
  plugin_stargazers_charts: no
  plugin_stargazers_worldmap: yes
  plugin_stargazers_worldmap_token: ${{ secrets.GOOGLE_MAP_TOKEN }}
  plugin_stargazers_worldmap_sample: 200

```
<!--/examples-->

<!--header-->
<table>
  <tr><td colspan="2"><a href="/README.md#-plugins">← Back to plugins index</a></td></tr>
  <tr><th colspan="2"><h3>📅 Isometric commit calendar</h3></th></tr>
  <tr><td colspan="2" align="center"><p>This plugin displays an isometric view of a user commit calendar along with a few additional statistics like current streak and average number of commit per day.</p>
</td></tr>
  <tr><th>⚠️ Disclaimer</th><td><p>This plugin is not affiliated, associated, authorized, endorsed by, or in any way officially connected with <a href="https://github.com">GitHub</a>.
All product and company names are trademarks™ or registered® trademarks of their respective holders.</p>
</td></tr>
  <tr>
    <th rowspan="3">Supported features<br><sub><a href="metadata.yml">→ Full specification</a></sub></th>
    <td><a href="/source/templates/classic/README.md"><code>📗 Classic template</code></a> <a href="/source/templates/terminal/README.md"><code>📙 Terminal template</code></a></td>
  </tr>
  <tr>
    <td><code>👤 Users</code></td>
  </tr>
  <tr>
    <td><code>🔑 (scopeless)</code> <code>read:org (optional)</code> <code>read:user (optional)</code> <code>read:packages (optional)</code> <code>repo (optional)</code></td>
  </tr>
  <tr>
    <td colspan="2" align="center">
      <details open><summary>Full year calendar</summary><img src="https://github.com/lowlighter/metrics/blob/examples/metrics.plugin.isocalendar.fullyear.svg" alt=""></img></details>
      <details><summary>Half year calendar</summary><img src="https://github.com/lowlighter/metrics/blob/examples/metrics.plugin.isocalendar.svg" alt=""></img></details>
      <img width="900" height="1" alt="">
    </td>
  </tr>
</table>
<!--/header-->

## ➡️ Available options

<!--options-->
<table>
  <tr>
    <td align="center" nowrap="nowrap">Option</i></td><td align="center" nowrap="nowrap">Description</td>
  </tr>
  <tr>
    <td nowrap="nowrap"><h4><code>plugin_isocalendar</code></h4></td>
    <td rowspan="2"><p>Enable isocalendar plugin</p>
<img width="900" height="1" alt=""></td>
  </tr>
  <tr>
    <td nowrap="nowrap"><b>type:</b> <code>boolean</code>
<br>
<b>default:</b> no<br></td>
  </tr>
  <tr>
    <td nowrap="nowrap"><h4><code>plugin_isocalendar_duration</code></h4></td>
    <td rowspan="2"><p>Time range</p>
<ul>
<li><code>half-year</code>: 180 days</li>
<li><code>full-year</code>: 1 year</li>
</ul>
<img width="900" height="1" alt=""></td>
  </tr>
  <tr>
    <td nowrap="nowrap"><b>type:</b> <code>string</code>
<br>
<b>default:</b> half-year<br>
<b>allowed values:</b><ul><li>half-year</li><li>full-year</li></ul></td>
  </tr>
</table>
<!--/options-->

## ℹ️ Examples workflows

<!--examples-->
```yaml
name: Half-year calendar
uses: lowlighter/metrics@latest
with:
  filename: metrics.plugin.isocalendar.svg
  token: ${{ secrets.METRICS_TOKEN }}
  base: ""
  plugin_isocalendar: yes

```
```yaml
name: Full-year calendar
uses: lowlighter/metrics@latest
with:
  filename: metrics.plugin.isocalendar.fullyear.svg
  token: ${{ secrets.METRICS_TOKEN }}
  base: ""
  plugin_isocalendar: yes
  plugin_isocalendar_duration: full-year

```
<!--/examples-->
