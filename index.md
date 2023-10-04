---
layout: page
---

{% assign people_sorted = site.people | sort: 'joined' %}
{% assign role_array = "pi|postdoc|grad|ugrad" | split: "|" %}

{% for role in role_array %}

{% assign people_in_role = people_sorted | where: 'position', role %}

<!-- Skip section if there's nobody -->
{% if people_in_role.size == 0%}
  {% continue %}
{% endif %}

<div class="pos_header">
{% if role == 'postdoc' %}
<h3>Postdoctoral Fellows</h3>
{% elsif role == 'pi' %}
<h3>Principal Investigator</h3>
{% elsif role == 'grad' %}
<h3>Graduate Students</h3>
{% elsif role == 'ugrad' %}
<h3>Undergraduate Students</h3>
{% endif %}
</div>

<div class="content list people">
  {% for profile in people_sorted %}
    {% if profile.position contains role %}
      <div class="list-item-people">
        <p class="list-post-title">
          {% if profile.avatar %}
            <a href="{{ site.baseurl }}{{ profile.url }}"><img class="profile-thumbnail" src="{{site.baseurl}}/images/people/{{profile.avatar}}"></a>
          {% else %}
            <a href="{{ site.baseurl }}{{ profile.url }}"><img class="profile-thumbnail" src="{{site.baseurl}}/images/people/missing_profile.png"></a>
          {% endif %}
          <a class="name" href="{{ site.baseurl }}{{ profile.url }}">{{ profile.name }}</a>
        </p>
      </div>    
    {% endif %}
  {% endfor %}
</div>
<hr>
{% endfor %}

<h3>Alumni</h3>

<ul>
<li><a href="https://www.linkedin.com/in/nabeel-hingun-044a40198">Nabeel Hingun</a> (<a href="https://hiddenlayer.com/">HiddenLayer</a>),
M.S., 2023,
<a href="https://www2.eecs.berkeley.edu/Pubs/TechRpts/2023/EECS-2023-153.html">Scaling Part Models: Challenges and Solutions for Robustness on Large Datasets</a>.
<li><a href="https://www.nathanmalkin.com/">Nathan Malkin</a> (U Maryland), Ph.D., 2021,
<a href="https://www2.eecs.berkeley.edu/Pubs/TechRpts/2022/EECS-2022-249.html">Privacy Controls for Always-Listening Devices</a>.
<li><a href="https://www.linkedin.com/in/an-ju-phd/">An Ju</a>, Ph.D., 2021,
<a href="https://www2.eecs.berkeley.edu/Pubs/TechRpts/2021/EECS-2021-47.html">Generative Models as a Robust Alternative for Image Classification: Progress and Challenges</a>.
<li><a href="https://www.linkedin.com/in/alan-rosenthal-37767614a/">Alan Rosenthal</a> (Dexterity Capital), M.S., 2021,
<a href="https://www2.eecs.berkeley.edu/Pubs/TechRpts/2021/EECS-2021-68.html">Improving the Efficiency of Robust Generative Classifiers</a>.
<li><a href="https://henryzxu.com/">Henry Xu</a>, M.S., 2021,
<a href="https://www2.eecs.berkeley.edu/Pubs/TechRpts/2021/EECS-2021-105.html">Model-Agnostic Defense for Lane Detection Against Adversarial Attack</a>.
<li><a href="https://www.linkedin.com/in/zhanyuan-zhang/">Zhanyuan Zhang</a>, M.S., 2021,
<a href="https://www2.eecs.berkeley.edu/Pubs/TechRpts/2021/EECS-2021-126.html">Towards Characterizing Model Extraction Queries and How to Detect Them</a>.
<li><a href="https://www.linkedin.com/in/zachary-golan-strieb-386b8a9b/">Zachary Golan-Strieb</a> (Duolingo), M.S., 2021,
<a href="https://www2.eecs.berkeley.edu/Pubs/TechRpts/2021/EECS-2021-241.html">Towards Evaluating and Understanding the Adversarial Robustness of Random Transformation Defenses</a>.
<li><a href="https://www.linkedin.com/in/michael-mccoyd/">Michael McCoyd</a>, Ph.D., 2020,
<a href="https://www2.eecs.berkeley.edu/Pubs/TechRpts/2020/EECS-2020-170.html">Background and Occlusion Defenses Against Adversarial Examples and Adversarial Patches</a>.
<li><a href="https://cseweb.ucsd.edu/~grho/">Grant Ho</a> (UCSD), Ph.D., 2020,
<a href="https://www2.eecs.berkeley.edu/Pubs/TechRpts/2020/EECS-2020-217.html">Thwarting Sophisticated Enterprise Attacks: Data-Driven Methods and Insights</a>.
<li><a href="https://www.linkedin.com/in/neil-shah-413216133/">Neil Shah</a> (<a href="https://www.workday.com/">Workday</a>), M.S., 2020.
<a href="https://www2.eecs.berkeley.edu/Pubs/TechRpts/2020/EECS-2020-80.html">A Large-Scale Analysis of Attacker Activity in Compromised Enterprise Accounts</a>.
<li>Steven Chen, M.S., 2019,
<a href="https://www2.eecs.berkeley.edu/Pubs/TechRpts/2019/EECS-2019-55.html">Stateful detection of black box adversarial attacks</a>.
<li><a href="http://nicholas.carlini.com/">Nicholas Carlini</a> (Google),
Ph.D., 2018, 
<a href="https://www2.eecs.berkeley.edu/Pubs/TechRpts/2018/EECS-2018-118.html">Evaluation and Design of Robust Neural Network Defenses</a>.
<li><a href="https://www.linkedin.com/in/rebecca-portnoff-3b784039/">Rebecca Portnoff</a> (<a href="https://www.wearethorn.org/">Thorn</a>),
Ph.D., 2018,
<a href="https://www2.eecs.berkeley.edu/Pubs/TechRpts/2018/EECS-2018-5.html">The Dark Net: De-Anonymization, Classification and Analysis</a>.
<li><a href="https://people.csail.mit.edu/thurston/">Thurston Dang</a> (MIT),
Ph.D., 2017,
<a href="https://www2.eecs.berkeley.edu/Pubs/TechRpts/2017/EECS-2017-209.html">Towards Improved Mitigations for Two Attacks on Memory Safety</a>.
<li><a href="https://notyetsecure.com/">Chris Thompson</a> (<a href="https://www.linkedin.com/in/cthompson5">Google</a>),
Ph.D., 2017,
<a href="https://www2.eecs.berkeley.edu/Pubs/TechRpts/2017/EECS-2017-217.html">Large-Scale Analysis of Modern Code Review Practices and Software Security in Open Source Software</a>.
<li><a href="https://www.linkedin.com/in/lynn-tsai-86421168">Lynn Tsai</a> (Google),
M.S., 2017,
<a href="https://www2.eecs.berkeley.edu/Pubs/TechRpts/2017/EECS-2017-44.html">TurtleGuard: Helping Android Users Apply Contextual Privacy Preferences</a>.
<!-- https://lynntsai.com/ !-->
<li><a href="https://www.linkedin.com/in/theodorides">Michael Theodorides</a> (Yahoo),
M.S., 2017,
<a href="https://www2.eecs.berkeley.edu/Pubs/TechRpts/2017/EECS-2017-78.html">Breaking Active-Set Backward-Edge Control-Flow Integrity</a>.
<li><a href="http://www.eecs.berkeley.edu/~lindanaeunlee/">Linda Lee</a> (Zcash),
M.S., 2016,
<a href="https://www2.eecs.berkeley.edu/Pubs/TechRpts/2016/EECS-2016-58.html">Tor's Usability for Censorship Circumvention</a>.
<li><a href="https://www.linkedin.com/in/arjunbaokar">Arjun Baokar</a>,
M.S., 2016,
<a href="http://www2.eecs.berkeley.edu/Pubs/TechRpts/2016/EECS-2016-69.html">

A Contextually-Aware, Privacy-Preserving Android Permission Model</a>.
<li><a href="http://www.linkedin.com/pub/sakshi-jain/a/702/149">Sakshi Jain</a> (LinkedIn),
M.S., 2014,
<a href="http://www.eecs.berkeley.edu/Pubs/TechRpts/2014/EECS-2014-229.html">Automated Discovery of User Trackers</a>.
<li><a href="http://cs.unc.edu/~csturton/">Cynthia Sturton</a> (UNC Chapel Hill), 
Ph.D., 2013,
<a href="http://www.eecs.berkeley.edu/Pubs/TechRpts/2013/EECS-2013-224.pdf">Secure Virtualization with Formal Methods</a>.
<li><a href="http://www.cs.berkeley.edu/~emc/">Erika Chin</a>
(Twitter),
Ph.D., 2013,
<a href="http://www.eecs.berkeley.edu/Pubs/TechRpts/2013/EECS-2013-58.pdf">Helping Developers Construct Secure Mobile Applications</a>.
<li><a href="https://mfinifter.github.io/">Matthew Finifter</a>
(<a href="https://www.linkedin.com/in/matthew-finifter-664929103">Uber</a>),
Ph.D., 2013,
<a href="http://www.eecs.berkeley.edu/Pubs/TechRpts/2013/EECS-2013-49.pdf">Towards Evidence-Based Assessment of Factors Contributing to the Introduction and Detection of Software Vulnerabilities</a>.
<li><a href="http://www.informatik.uni-trier.de/~ley/pers/hd/m/Mettler:Adrian.html">Adrian Mettler</a>
(Fireeye),
Ph.D., 2012,
<a href="http://www.eecs.berkeley.edu/Pubs/TechRpts/2012/EECS-2012-244.html">Language and Framework Support for Reviewably-Secure Software Systems</a>.
<li><a href="http://www.adrienneporterfelt.com/">Adrienne Porter Felt</a>
(Google),
Ph.D., 2012,
<a href="http://www.eecs.berkeley.edu/Pubs/TechRpts/2012/EECS-2012-185.pdf">Towards Comprehensible and Effective Permission Systems</a>.
<li><a href="http://www.dero.org/">Arel Cordero</a>,
Ph.D., 2010:
<a href="arel-phd.pdf">Enabling More Meaningful Post-Election
Investigations</a>.
<li><a href="http://www.dmolnar.com/">David Molnar</a>
(Microsoft Research),
Ph.D., 2009:
<a href="dmolnar-phd.pdf">Dynamic Test Generation for Large Binary
Programs</a>.
<li><a href="http://www.chriskarlof.com/">Chris Karlof</a>
(Mozilla),
Ph.D., 2009:
<a href="http://www.eecs.berkeley.edu/Pubs/TechRpts/2009/EECS-2009-26.pdf">Human Factors in Web Authentication</a>.
<li><a href="http://www.quarl.org/">Karl Chen</a> (D.E. Shaw), 2008.
<li><a href="http://zesty.ca/">Ka-Ping Yee</a>
(<a href="https://www.wave.com/">Wave</a>),
Ph.D., 2007: <a href="yee-phd.pdf">Building Reliable Voting
Machine Software</a>.
<li><a href="http://naveen.ksastry.com/">Naveen Sastry</a> (McKinsey),
Ph.D., 2007: <a href="sastry-phd.pdf">Verifying Security Properties
in Electronic Voting Machines</a>.
<li><a href="http://umeshshankar.com/">Umesh Shankar</a> (Google).
Ph.D., 2006: <a href="ushankar-phd.pdf">Bridging the Gap between People
and Policies in Security and Privacy</a>.
<li><a href="https://research.vmware.com/researchers/rob-johnson">Rob Johnson</a>
(VMWare).
Ph.D., 2006: <a href="rtjohnso-phd.pdf">Verifying Security Properties
using Type-Qualifier Inference</a>.
<li><a href="http://www.cs.ucdavis.edu/~hchen/">Hao Chen</a> (U.C. Davis).
Ph.D., 2004: <a href="hchen-phd.ps">Lightweight Model Checking
for Improving Software Security</a>.
<li>Jason Waddle (Google).
M.S., 2004: <a href="jwaddle-ms.ps">Formalizing Secure Computation
for Embedded Systems</a>.
<li>Ben Schwarz,
M.S., 2005: <a href="bschwarz-ms.pdf">Model Checking An Entire
Linux Distribution for Security Violations</a>.
</ul>