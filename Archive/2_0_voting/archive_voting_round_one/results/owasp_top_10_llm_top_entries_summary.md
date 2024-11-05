# Summary of Top Entries for OWASP Top 10 LLM

## PromptInjection

**Total Votes:** 47

### Justifications:

- Definitely the biggest problem facing LLMs at this time. Seeing the rise of guardrails and output protection. 

- IMHO this is the TOP-1 vulnerability and that should stay like this.

- This is IMO the top new class of risks introduced by LLM usage in apps.   If anything it could be rolled under injection attacks, but in the context of LLMs it feels like a top-level entry.

- This should remain the Number one - continue education on the various styles and approach to prompt engineering should be considered.  examples: UPIA, Role Play, Crescendo and Many-Shot Jailbreaking (MSJ)

- Still the first and biggest attack vector for most people

- Prompt injections allow end users to manipulate LLMs in malicious manners, to reveal sensitive info etc. It can be considered a type of adversarial input.

- This one and “adversarial inputs” could be combined. I think this one needs some attention and rewrite to be more inclusive of what we now know.

- Content Control: Controlling and moderating the content becomes challenging if the model can be directed to output inappropriate or harmful text.

- I think the intentional vs unintentional is actually important to account for here, as well as a lot of other suggestions such as adversarial input and so forth could be captured with a significant rewrite of this.

- Importance: Prompt injection attacks mess with LLM inputs to change how they behave, which can lead to unauthorized actions and data leaks. It's crucial to make sure LLMs handle inputs securely to maintain trust and reliability, especially since these models are used in everything from chatbots to finance and healthcare.

Top-Level Entry or Folded: This deserves its own top-level entry because it has a wide impact and presents unique challenges that need specific defenses and awareness.

Additional Thoughts: We should keep an eye on evolving threats, encourage collaboration between AI and cybersecurity experts, and provide training on how to spot and prevent these attacks to boost overall AI security.


## DangerousHallucinations

**Total Votes:** 33

### Justifications:

- Although guardrails are being put in place in Transformer Decoder systems such that the decoder does not let its imagination run wild, there is still a whole lot of work that needs to be done in preventing hallucinations. The very nature of a transformer decoder system is to 'generate text' (accurate information or not). It is its nature, so it is up to us to stop it from generating text that is factually incorrect. Wrong/inaccurate information generated can produce huge losses and heartburn to companies that take the LLM's output as trusted and even automate their systems to act based on LLM outputs!

- could be folded into other hallucinations but deserves special attention due to overreliance of users.

- Hallucination is one of the corner pieces of generative AI - hate it or love it. So it should be a 1st class citizen in the Top n LLMs. I think the title should be Hallucination & Emergent Behavior. Emergent Behavior is hallucination++, more important in the world of agents - planning et al. 
Second, need to add the view that hallucination is not something that needs to be totally eradicated. So Dangerous Hallucination should be one of the sub elements. May be Contextual Hallucination might be the right title. One reason is that, to get the real value out of Gen AI we need to embrace Hallucination and Emergent behavior (see https://bit.ly/gen-ai-org-surgery, https://bit.ly/hallucination-is-a-feature)
As many of the characteristics depend on the context a catch-all guardrail suppressing hallucination is not a valid solution. For example, while hallucination is not good for deterministic apps, it is an essential component for creative apps like drug discovery, protein folding, marketing, recommendation and so forth

- Dangerous Hallucinations are the number one risk of Generative AI applications. Hallucinations lead to misinformation, loss of brand trust, and in some cases, has caused high profile PR disasters. The risk is exacerbated by the fact that well-tuned LLMs have high confidence in their predictions, and therefore always sound confident. Therefore, we believe that hallucinations should be a new, top level entry as opposed to folded into a larger vulnerability.

- It should be new a top-level entry. This is a very common vulnerability, and certainly one that developers should put effort into addressing as early as possible.

- The usability of a model comes down, at the end of the day, to trust in its responses. Limiting hallucinations will not only raise the trust in the model, but will also avoid silly humans doing silly things based on an hallucinated recommendation.


- Exploitation Potential: Malicious actors could manipulate the model to generate harmful or dangerous instructions.

- Common people see LLM as a magical way to have correct answers. Clearly identifying the dangerous hallucinations risk can lower the development of applications without hallucinations protections

- The most concerning security issues show up even when users are behaving "normally". Model hallucinations are like this, and it's especially concerning when they can be dangerous - leading users to believe the wrong things or take the wrong actions.

- Dangerous hallucinations in AI systems represent a significant concern due to their potential to generate false, misleading, or harmful information. This issue is critical for several reasons: it can lead to the spread of misinformation, causing public confusion or panic, financial losses, or harm to individuals and society. Ensuring that AI outputs are accurate and trustworthy is essential for maintaining user trust and confidence in AI technologies. Addressing dangerous hallucinations could be considered a top-level entry because it involves specific technical challenges and ethical considerations related to AI's capability to generate and disseminate information. Effective mitigation strategies include developing robust detection mechanisms for harmful outputs, educating users about AI capabilities and limitations, and implementing regulatory frameworks to promote responsible AI deployment. Whether tackled independently or integrated into a broader vulnerability framework, mitigating dangerous hallucinations is crucial for fostering ethical and reliable AI applications in society.


## BypassingSystemInstructionsUsingSystemPromptLeakage

**Total Votes:** 32

### Justifications:

- Leaking system prompt can have quite a significant affect on the organisation.

- While this is seemingly a "fad" entry, the fact is several agent hosting industries have been hit with this where their IP was exposed as a result. I would therefore rank this as another top level consideration to ensure any organization is aware of the risk and preferably provided with actionable guidance

- folded into other prompt exploitation vulnerability

- Any system bypasses need to be prioritized, no matter how small they may appear on the surface.  The next attack vector may be easier to get to.

- Hi-jacking the model in this way threat actors can create dangerous implements that can cause harm.


## SupplyChainVulnerabilities

**Total Votes:** 29

### Justifications:

- The explosion of open access models and weighs make this a must inclue

- Malicious libraries, Model serialization attacks, biased models from 3rd parties

- Once these vulnerabilities are in, it will be harder to remove. Solarwinds on steroid

- LLM supply chain vulnerabilities refer to security risks and weaknesses that can occur at various stages of an LLM's development, deployment, and use. This includes security in data collection, cleansing, preparation. Security in model training, model access control. Model Distribution such as tampering with various parameters. (if temperature, top k / p available to end user)  - In Deployment - Insecure API access to the model or data used by the model.

- So much churn in new 3rd party AI libraries that're pulled into application dependency graphs. 

- If we see the OWASP LLM Top 10 as a graph, 'Supply Chain Vulnerabilities' might be the root node. This is because it involves multiple layers of security measures, thorough vetting of third-party components, continuous monitoring for vulnerabilities, and adherence to best practices and standards throughout the entire development lifecycle. Additionally, it concerns how users interact with the product on a daily basis.

From this root node, other vulnerabilities branch out, interconnected by their dependence on a secure supply chain. Issues like 'Training Data Poisoning' and 'Insecure Plugin Design' highlight specific risks within the broader supply chain, emphasizing the importance of maintaining robust security practices at every stage to prevent cascading effects that compromise the entire system.

- With the introduction of the LLMs within almost every current Software/Vendor provider. The landscape has changed and become more complex; this includes the trust of a 3rd parties LLMs to a web of APIs to be managed and secured.  Additionally, as cyber warfare has been a traditional approach, supply chain attacks have become a main approach in the model world. 

- Software that supports building and managing AI systems has not been designed to be secure

- Great addition to the existing item.

- Because of the rapid changes due to LLM advancements, there is a constant need to maintain and update the modules and APIs around AI as the mechanism engine to incorporate (because they can suddenly end their lifetime). This is a level of change that was not present in other third-party components such as OSS.


## SensitiveInformationDisclosure

**Total Votes:** 29

### Justifications:

- With many organisations pushing as much internal info as possible form knowledge bases into RAG solutions the permission scheme from the origin system is lost and potentially all end users might have access to all RAG information, if they ask the right questions.

- Sensitive Information Disclosure is an umbrella term that encompasses other issues, such as Model Theft, which are shared scenarios of data exfiltration. It even covers Privacy Violation.

- Leaked sensitive information is never good

- Sensitive Information includes PII leakage (emails, phone numbers etc.), PHI (medical IDs) or business sensitive information (see Patronus AI's enterprise PII dataset). This is important as it poses a huge risk to businesses. Sensitive data risks is a standalone category as it encompasses many different kinds of private and personally identifying information.

- More and more models are trained with highly proprietary and focused datasets, who need to be protected accordingly. As well, agents may have access to databases and other sources of sensitive data, and they should have the protection of sensitive information as one of their guiding values.

- the side-channel aspect about the predictability leading to weakening of encryption I think is an important one and not captured in previous versions. while people think of the traditional sort of way that sensitive information could be leaked by a bot through jailbreaking or prompt injection, this is very different and specific to encryption of data which is a huge security risk

- I think it is important because information privacy policies must be maneuvered with caution and caution. precisely because the data can be exposed and must be prevented.

- Sensitive information disclosure is a broad category which includes training data and data that happens using LLMs. 

- Models should minimize the amount of sensitive information used any way. The fact that would be able to be for disclosure is dangerous. It’s very bad if the LLM can disclose server secrets like keys and passwords 

- SENSITIVE INFORMATION DISCLOSURE should merge these entries = PrivacyViolation + SensitiveInformationDisclosure + ModelInversion + EmbeddingInversion


## BackdoorAttacks

**Total Votes:** 22

### Justifications:

- This is the major concern of many, if we are talking about LLM adoption in sensitive environments this is one of the major threats

- Training process has to be strictly monitored. Open source models are very vulnerable to these kind of attacks especially.

- Should be included into Supply Chain attacks

- Backdoor attacks are always userful.

- Similar to choice 3

- Without proper control of your system you are left at the will of the intruder.

- Importance: Backdoor attacks involve inserting hidden malicious functionality into AI models, which can be triggered under specific conditions. This poses a significant threat as it can lead to unauthorized actions and data breaches, compromising the integrity and security of AI systems.

Top-Level Entry or Folded: This should be a new, top-level entry because of the severe impact and unique challenges backdoor attacks present. They require focused strategies for prevention and detection.

Additional Thoughts: Ensuring secure training processes, continuous monitoring for suspicious behavior, and collaboration between AI developers and cybersecurity experts are key to defending against backdoor attacks. Education on recognizing and mitigating these threats is also crucial for maintaining secure AI systems.

- Backdoor attacks in large language models enable attackers to insert hidden, malicious functionalities that can be triggered later to compromise the system, leading to data theft, unauthorized access, and manipulation of outputs. These attacks are particularly dangerous as they can remain undetected for extended periods, undermining the security and trustworthiness of AI applications. Should be included as Top-level in the OWASP Top 10 emphasizing the critical need for rigorous code audits, anomaly detection, and validation processes to identify and mitigate hidden threats, ensuring the robustness and integrity of AI systems.

- Important that we don't only focus on the integration side of LLMs but the training/finetuning side also. Can be merged with v2 candidates #18 Malicious LLM Tuner. 

- At least half of the top 10 should be dedicated to protecting the actual behaviour of models - those things that are uniquely AI security and require non-traditional controls.


## DeepfakeThreat

**Total Votes:** 22

### Justifications:

- it is specific, easy to understand, and most worrisome and wide spread threat with LLM. 

- Its prevalence and imapct

- This is a serious threat that AI poses 

- Fraud and Impersonation: Deepfakes can be used for fraudulent activities, such as impersonating individuals for financial gain or unauthorized access. Similar to the deepfake threat in Feb 2024 when the finance worker pays out 25Mil in video scam.

- With the rise of multimodal LLMs, application protection against deepfakes will be important. Impact is huge with fraud and many systems will be vulnerable. Should be top level item

- Deepfakes may be used for Phishing. 

- Most systems are ultimately protected by people - and being able to create a fake representation of a person could break many contemporary security paradigms.

- Obviously the mass manipulation of humans

- It's incredibly dangerous to live in a world where we can't tell the truth from the falsehoods. Deepfake is a step towards that world.

- Deep Fakes represent large threats to how information is shared. Easily spotting them is going to be key. 


## Unwanted-AI-Actions.md

**Total Votes:** 21

### Justifications:

- Many of our LLM use cases are centered around addressing information needs about a specific topic or expertise. By using 'general purpose LLMs' for specific tasks, there is a huge risk of false/inaccurate information from being output by the LLMs, leading to losses (financial and legal).

- First of all - this is my own submission so this response might be biased.
From the regulatory pressure - explicitly across hundredths of jurisdictions - this is one of the main issues I often see. For example: In Germany it is illegal to provide insurance advice if you are not a trained professional - hence a AI model must not do that.

- Unwanted AI actions can cover a wide range of undesirable day to day AI scenarios.

- It should be new a top-level entry. This is a very common vulnerability, and certainly one that developers should put effort into addressing as early as possible.

- This touches on alignment in an interesting fashion: alignment in terms of what organizations want their LLM apps to do (and not do). I believe it's fundamentally important and practical because unalignment can lead to legal issues, brand damage, privacy violations, etc.

- Focuses on the repercussions of AI systems executing unintended actions, which can lead to significant legal and reputational consequences. Given the complexity of these issues, it merits a distinct category to address configuration and validation lapses.


## InsecureDesign

**Total Votes:** 21

### Justifications:

- Inaccurate knowledge about AI systems while designing them is a top reason for security-related incidents.

- Self explanatory 

- Insecure design in Large Language Models (LLMs) refers to vulnerabilities or flaws in the model's architecture, training, or deployment that can lead to security risks. Lack of input filtering, lack of output validation, supply chain, 3rd party plugins and API connection (RAG), improper training, Inadequate access control for both data from LLM, access to llm, appropriate monitoring and logging, Security event generation can all be part of Insecure Design. 

- I think the "Insecure Design" issue really goes beyond the plugin concerns. It may involve the following:

- Failing to clearly define the LLM's purpose, use cases, and target audience.
- Not establishing clear metrics for success or evaluation criteria.
- Lacking a security threat modeling according to the system's goals

- It all begins at design, and threat modeling has historically been a neglected activity for many reasons. With CISA making a hard push for security-by-design and security-by-default, it makes sense that the fastest, largest area of development, and one that will no doubt have far reaching consequences on society, should receive security attention from the design step forward.

- Unintended Behaviors: Insecure design can result in unpredictable or harmful outputs, compromising the model's reliability.

- LLM design is hard, especially in absence of well-known best practices. Acknowledging this is a problem is important

- Insecure design in large language models leads to vulnerabilities that can be exploited by attackers, resulting in data breaches, unauthorized access, and manipulation of AI outputs. It undermines the reliability and trustworthiness of AI applications, posing risks to both users and organizations. Including insecure design in the Top 10 highlights the importance of integrating robust security measures from the outset, ensuring that AI systems are built to withstand threats and protect sensitive information. Top-level.

- This is core to app security, and being brushed over in AI Applications.

- The base to any attack or misuse


## VulnerableAutonomousAgents

**Total Votes:** 20

### Justifications:

- An emerging area that will redefine Generative AI, a natural step towards AGI we need to cover

- Agents are becoming relevant and need to be addressed at the top level. Planning and action is not at all easy and so this will grow exponentially. We caan combine this with Agent Autonomy Escalation

- Super tricky

- As a first and foremost non-obvious problem/vulnerability of LLMs is that an attacker can in may ways manipulate or control the output of the LLM so we MUST use the output as an untrusted text like if it was an internet exposed free text form

- should be a new, top-level entry or folded into another larger vulnerability as a concept.

- The consequences of agents are yet to be discovered. It would be great to discuss if multi-agent systems should be part of this as well.

- The concept of "Autonomy" in agentic development implies the use of canonical instructions and function callings that rely on the environment and infrastructure. Being this aspect very likely unrelated to the AI/ML team but potentially assigned to a localized team that develops actions mechanism, I see a strong risk that is confirmed inthe LowCode NoCode top10. I vow for this. Agentic dev is the next big thing.

- i think the name is too generic, but there should be definitely entry on agents; the other entry on agent escalation should be folded here

- Excellent and well researched entry beyond the usual general worries about autonomy

- I don't like the name of this one.  The vulnerability is that they're vulnerable?  But the concept of covering the specific vulnerabilities related to agents is critical.  We should explore further.


## MultimodalInjections

**Total Votes:** 20

### Justifications:

- where we face multi modal model this could be an issue

- Could be bundled to other prompt injections but probably deserves special status due to complexity

- Increased attack and failure vector 

- With the introduction of models like GPT 4o, the landscape has expanded beyond just text to new novel attacks crossing various conversions, like voice-to-text then text-to-visual. 

- I think this is a new one.

- I think most AIs will be multimodal soon, and this is an important vuln not previously captured

- This is a reflection of steganography and steganophony attacks that I have seen used very much with the GPT-4o and more models. it requires specific filtering approaches and would be a good wake up call. I've always advocated to the fact that encrypting data and watermarks is easier when data is denser, and this captures the concept.

- i am not sure if this should be part of prompt injection or different, but it will become an issue as genAI systems become more complex. a variant of this is also LLM chaining (where some LLMs are used as protective controls in the flow of transactions - eg using ML model to mask data or to evaluate if the prompt is broken)

- Excellent entry but we should make this part of the existing

- A fundamental attack vector that LLMs and MLLMs are fundamentally weak against. I'd consider it a superset of all the other injections mentioned in the list.


## FunctionCallingAttack

**Total Votes:** 17

### Justifications:

- function.call can have Security implications

- This is one of the most common issues I see on a daily basis with customers. So this a great fit for number 2.

- Importance: Function Calling Attacks (FCA) pose significant risks by exploiting LLMs’ ability to execute external functions, leading to unauthorized access, data breaches, and system manipulation.

Top-Level Entry: FCAs should be a new, top-level entry due to their unique nature and specific mitigation needs, distinct from other vulnerabilities.

Additional Thoughts: Implement advanced monitoring and detection, conduct regular security assessments, promote collaboration for knowledge sharing, and develop clear policies and best practices to minimize FCA risks.

- By linking this item with lowcode nocode top10 items I see the potential for this to grow and proliferate. Function calling is a distinct and intermediate way to access enhanced functions and I think this way of describing what was a "plugin" denomination before is more suitable to distinct from agents and agentic llm dev.

- As chatbots gain more power - like being able to call functions and change the behavior of downstream services - it greatly expands the risk profile of LLMs. They are now not just ferrying text in and out, but affecting change in downstream systems.

- This is a great entry but most probably needs to be part of injections instead of a new entry 

- Function calling attacks in large language models allow malicious actors to exploit the model's ability to execute or call functions, leading to unauthorized actions, data breaches, and system manipulation. These attacks can compromise the integrity and security of AI applications, making them vulnerable to exploitation. Including in the Top-level Top 10 underscores the need for stringent validation, monitoring, and control mechanisms to prevent unauthorized function execution and ensure the safe operation of AI systems.


## InsecureInputHandling

**Total Votes:** 16

### Justifications:

- Insecure Input handling covers various adversarial inputs, prompt injection, prompt extraction and prevent sensitive information disclosure by avoiding prompts that are susceptible to these attacks.  It helps with Security, Output integrity, Privacy protection, ethical use of AI, system availability.  "Prompt injection could be part of input validation, however more robust protection is required to allow prompts that are valid and prevent that are not valid. LLMs interpret natural language, making validation more complex than traditional input sanitization. The goal is to prevent the model from executing unintended instructions or revealing sensitive information

- I actually like the idea of maybe having a broader split of the vulns around input and output, and I feel like this is a step in the right direction. If we had a top 10 for each side, how models handle inputs and outputs and the vulns within them, we could cover more problem space and help the community more

- Related to Indirect Prompt Injection and also vulnerabilities in Agentic System, recommend this as the base vulnerability that can incorporate the problems with insecure data being ingested by an LLM


## AgentAutonomyEscalation

**Total Votes:** 16

### Justifications:

- This feels like it's part of the same category as UnauthorizedAccess but worth calling out separately because agentic workflows are such a common design pattern

- The expansion from chains to Autonomous agents, the risk of either the agents misused with malicious intent or agents have over-permissions either through misconfiguration or the lack of understanding of the capabilities of autonomous agent.  It could result in any from date loss, corrupt or self-inflicted DoS of some other system or infrastructure.

- Real time  attacks seen

- This is a direct consequence of Insecure Design. Providing the ability for an agent to autonomously perform sensitive operations should be a high cost, high justification activity not taken lightly, and all ability to escalate that autonomy should be hardened or, ideally, prevented lest the agent incur in unwanted or damaging behavior.

- There is a widespread lack of understanding of how Generative ML use, leading to extremely dangerous misuses - be it wrt cyber-offensive operations or actual societal damaage.

- The feature demand for LLM-based software call for features that interact with other applications or devices. As this advances, there's a big risk user will abuse the software to try and enact behaviors they should not be allowed to.

- Needless to say, attributing roles and privileges to agents and to the model itself when function calling happens are both critical and since the enterprise is thirsty about having automation happen I think this gains importance. The initial hype of LLM models Q&A is crossed and the next step is to see  it act by solving real issues, agents are exactly that.

- Agent autonomy escalation occurs when an AI system gains more control or makes decisions beyond its intended scope, potentially leading to harmful outcomes. This issue is crucial for risk management, trust, safety, and ethics, as unchecked autonomy can result in unpredictable and dangerous behaviors. It could be a top-level entry due to its unique challenges related to AI control and oversight, requiring specific strategies to monitor and manage autonomous agents. Alternatively, it can be integrated into a broader AI vulnerability framework for a comprehensive risk management approach. Effective handling of this issue demands interdisciplinary collaboration, continuous monitoring, and clear accountability structures. Whether treated independently or as part of a larger framework, agent autonomy escalation is vital for the safe and ethical deployment of AI systems.

- Agent autonomy escalation in large language models poses significant risks including unintended actions, security breaches, and exploitation by malicious actors. It complicates accountability and adherence to policies and regulations, while also potentially leading to biased and unethical decisions due to reduced human oversight. By including it in the Top-level at the LLM Top 10, we emphasize the critical need for effective controls and monitoring to manage these risks, ensuring AI applications are secure, compliant, and ethical.

- I think a major challenge with autonomous agents is access control. Once the agent has access to the file system, additional tooling, and the internet, crossing these access boundaries can lead to dangerous outcomes.


## AdversarialInputs

**Total Votes:** 15

### Justifications:

- I like the term 'Adversarial Inputs.' It could be a broad umbrella covering many other scenarios, from Prompt Injection to Data Poisoning. Borrowing the idea of characteristics and sub-characteristics of a quality model such as the ISO 25010, 'Adversarial Inputs' could be the equivalent of a characteristic involving several sub-characteristics related to different stages of user interaction with the LLM

- Production Scale  attacks  seen with this  approach 

- Adversarial inputs encompass any kind of user input that is intended to "break" the LLM. It can be considered in the same category as prompt injection.

- It should be new a top-level entry. This is a very common way to attack models, and certainly one that developers should put effort into addressing as early as possible.

- Importance: Adversarial inputs are crafted to trick AI models into making mistakes, which can lead to serious consequences in areas like healthcare, finance, and security. Ensuring AI models can handle these inputs is crucial for their reliability and safety.

Top-Level Entry or Folded: This should be a new, top-level entry because of its unique and significant impact, requiring specific strategies for detection and mitigation.

Additional Thoughts: Regular monitoring and updating of defenses, collaboration between AI and cybersecurity experts, and training on recognizing these attacks are essential for enhancing AI security and reliability.

- There are two categories of Adversarial Inputs - one category are clearly harmful, and effective classification on inputs can protect the LLM from having to process them. The more worrying variety are adversarial inputs that seem innocuous but generate harmful LLM behavior. We don't have any good models right now of these kinds of inputs, and if an attacker discovers them, it could be very dangerous.

- This can be folded with existing LLM01: Prompt Injection from v1.1 as both vulnerabilities use the same pathways with very similar objectives + v2 Candidate #28 System Prompt Leakage.

- At least half of the top 10 should be dedicated to protecting the actual behaviour of models - those things that are uniquely AI security and require non-traditional controls.


## ResourceExhaustion

**Total Votes:** 14

### Justifications:

- Could change denial of service and combine both of the entries into one. 

- Could be added into DoS as a sub category. Also linked to Unrestricted Resource Consumption. 

- Too many odd things happen when resources aren't controlled properly.

- High Computational Demand: Large language models require significant computational resources, which can be targeted to cause Denial of Service (DoS) by overwhelming the system.

- This is a highly relevant and yet underappreciated vector of attacks

- I like combination of both threats into single item

- Similar to a DOS attack but using the system against itself

- This is an improved version of our current Denial of service entry.  Including denial of wallet is crucial.

- This can be an extension to LLM04: Model Denial of Service

With LLMs becoming more widely deployed and used via APIs the cost of each request is becoming more apparent to many companies who are relying on the foundation models.

These costs can wrack up pretty fast, and even more than that an attacker can use the same tactics that are currently described in LLM04 to grow the vulnerable company's bill to enormous amounts quite easily

With more and more unaware developers deploying LLM applications and making them publicly available, awareness to how an attacker can overwhelm both the LLM and the company's bank account should become a top priority to anyone involved

- We are seeing more Objective being the resources used to run LLMs. Can be merged with v2 candidate #31 Unrestriced Resource Consumption.


## AdversarialAIRedTeamingCyberOps

**Total Votes:** 13

### Justifications:

- This definitely very important 

- SecOps is the way to go else we run the risk of good old days

- In today's world, APTs are conducting sophisticated offensive operations including creating deepfakes, spreading misinformation, and conducting cyber warfare. As the OWASP LLM authority it is up to us to ensure we help enterprises understand the risk involved and how they can mitigate it.

- Importance: Adversarial AI Red Teaming involves simulating attacks to identify and mitigate vulnerabilities in AI systems, crucial for improving resilience against real-world threats.

Top-Level Entry: This should be a new, top-level entry due to its specialized focus on proactive security testing and unique techniques used in AI adversarial attacks.

Additional Thoughts: Develop dedicated teams for continuous testing, create robust frameworks for adversarial simulations, collaborate across industries for best practices, and integrate findings into AI development lifecycles for enhanced security.

- AI red teaming is crucial for uncovering vulnerabilities in AI systems before malicious actors can exploit them. This proactive approach enhances the robustness and security of AI technologies, ensuring they can withstand and recover from attacks. Additionally, AI red teaming helps meet regulatory requirements, builds trust with users, and ensures ethical operation by identifying and mitigating potential harms. While AI red teaming could be a top-level entry due to its specialized nature requiring expertise in both AI and cybersecurity, it can also be integrated into a broader vulnerability management framework for a holistic approach to system security. Effective AI red teaming relies on interdisciplinary collaboration, continuous testing, and transparent reporting to improve industry standards and foster a culture of shared learning. Whether as an independent discipline or part of a larger framework, AI red teaming is essential for the safe and ethical deployment of AI technologies.

- Fundamentally dangerous because the damage can be far more widespread and many magnitudes more significant than traditional cybersecurity exploits.

- This entry addresses the strategic exploitation of AI in cyber offensives, highlighting its role in misinformation and cyber warfare. Its relevance to national security and evolving cybercrime tactics justifies a standalone category.


## DevelopingInsecureSourceCode

**Total Votes:** 12

### Justifications:

- Security is always important

- Code assistants usage is most common in cases where the user does not have the competences to evaluate it. LLMs are known to generate vulnerable code and so far were not patched for it. With pressure to have higher output with LLMs, we are effectively carpet-bombing codebases with vulnerabilities to go 10% faster, that we will have to pay later down the line with 10x refactor overhead.

- Many companies are already using copilots or LLM-based tools for code generation. Memorization or insecure code injections are important security concerns for the new generation of LLM-written apps. Top level item I think

- The candidates most prone to have their code written by a LLM are also the ones least probably to verify security issues with it.

- Developing insecure code combined with overreliance on AI can lead to vulnerabilities in resulting programs. 

- Developing insecure source code in large language models introduces vulnerabilities that can be exploited by attackers, resulting in data breaches, unauthorized access, and compromised system integrity. Poor coding practices increase the risk of introducing flaws that undermine the security and reliability of AI applications. It shows the importance of adopting secure coding standards, regular code reviews, and automated security testing to ensure that AI systems are built on a foundation of robust and secure code.

- a complete new attack vector that is not covered

- My response is slightly different than the given description of this entry choice, however, I didn't see a better fit among the choices.

This one can be combined with:
DangerousHallucinations
ImproperErrorHandling
InsecureInputHandling
Overreliancerewrite

This is an enormous issue because many coders, beginner and advance alike, are using GenAI for help with their coding. The problem is that most great coding makes up a very small percentage of the coding population. There is much more bad code than good code because it takes years of experience and often large coordinated teams. Even then bugs are introduced in the code. The issue is that GenAI models work on a statistical basis. The code used is the code that is "used on average" and that code is generally no the ideal code base.




## SystemPromptLeakage

**Total Votes:** 11

### Justifications:

- I believe this is a new vector that could expose critical information about the bots original purpose, and aid an attacker in crafting more specific attacks. 

- As soon as I know the system prompt, I can force it into DAN mode with some prompt engineering

- The system prompt may have rules and boundaries and sometimes sensitive information that not all users should be exposed to. 

- System prompts may contain sensitive information, which could leak. 

- So many hacks seem to start here.  With leakage of, or overwriting the system propt.

- This should be a new, top-level vulnerability

With LLM applications starting to contain much more context and information in the system prompt its leakage is becoming more and more dangerous. 

For example Custom GPTs (In the GPT store) contain the knowledge files contents in the system prompt (or the actual location in the VM to access the file). An attacker revealing this system prompt can fetch all the knowledge of the GPT.
In the same Custom GPTs, the system prompt also contains the actions (i.e. APIs) that the GPT can use, and those can also be uncovered by an attacker extremely easily.

With everyone building system prompts, and being completely unaware of the dangers while they're building them, system prompts are becoming bigger, more precise, and contain more and more information which can be incredibly sensitive. (like APIs, functions, and knowledge). It is our responsibility as a community to raise awareness to the dangers that those system prompts are exposed to.

In addition, if a system prompt is leaked it can easily be used to craft all sorts of elaborate prompt injections (direct & indirect) which will be much more robust and focused then the general ones.
For example an indirect prompt injection can be made incredibly robust by mentioning something the LLM saw in its system prompt (like a certain function it can use) to let the LLM know that this content is actually instructions.
This makes the system prompt a coveted prize every attacker would love to get their hands on.

The web is full of examples of leaked system prompts, its time to raise awareness to this vulnerability


- This can be combined with 
AdversarialAIRedTeamingCyberOps
BypassingSystemInstructionsUsingSystemPromptLeakage
SupplyChainVulnerabilities

In the future, breach data will be used to for enumeration and offensive security ops. Adversaries will be able to query what security controls an organization has in place. They'll be able to learn how contractors are connected and interact with a target company. This could also be done by adding the breached data of a company's partner to understand how they communicated with their partner company, the real target. 

If the breached data includes security logs or reports of audits, past investigations, or even daily notable closures, they could use a GenAI to give them the weaknesses based on those reports. This could give any adversary the tools and knowledge to drastically up their game.


## EmbeddingInversion

**Total Votes:** 11

### Justifications:

- There are tons of new vendors happy to store your vector embeddings, but most/all do not have a built in story for encrypting embeddings (using a distance preserving algo).  Which creates a brand new avenue for PII leakage :(

- There are custom embedding models which are creating 1) Embedding Membership attack  , 2) Embedding Inversion attack. 

- I don't think enough attention is given to the risk of extracting data from enbeddings. I think that the prevalence of RAG workflows and other tools that leverage embeddings mean the attack surface could be very large.

- new top level entry; it is inherent to genAI architectures (but different in nature from LLM01) and a high-impact due to sensitive data leakage risk

- This a misunderstood and ignored entry so I welcome this candidate 

- Embedding inversion, the process of reversing an embedding to retrieve original input data, poses significant privacy and security risks. It is crucial for data privacy, as it can expose sensitive information and undermine protections for individuals. Additionally, it presents security risks, allowing attackers to reconstruct confidential or proprietary data, leading to potential breaches and misuse. Protecting embeddings from inversion is essential for maintaining the integrity and trustworthiness of AI models. Embedding inversion could be considered a top-level entry due to its specific technical challenges and risks, requiring specialized techniques to secure embeddings against such attacks. Alternatively, it could be integrated into a broader AI vulnerability framework for a comprehensive risk management approach. Effective solutions demand advanced encryption methods, interdisciplinary collaboration between AI researchers, security experts, and privacy advocates, and continuous assessment to keep pace with evolving threats. Whether treated independently or as part of a larger framework, embedding inversion is a critical issue that must be addressed to ensure the privacy, security, and integrity of AI systems.

- ModelInvesion (related to training data) and the other entry on EmbeddingInversation are covering seperate topics that I think we should combine into one topic about using Inversion attacks to exfiltrate data from the app.

- I think there is value in merging this with v2 candidate #19 Model Inversion


## FineTuningRag

**Total Votes:** 10

### Justifications:

- The RAG/finetuning component is another corner piece of generative AI - and requires to be a first class citizen.

- LLMs are getting synonymous with RAG hence too dependent

- It should be new a top-level entry, or it could be rolled into Training Data Poisoning. This is a more domain/architecture-specific attack, but still important to keep in mind.

- A new, top-level vulnerability

As RAG & Finetuning (RAG especially) become more popular, new vulnerabilities are being discovered. RAG poisoning for example is an important one, an attacker can easily mislead a user by simply sending them a simple file.

RAG also presents dangerous indirect prompt injection attacks  which can mislead the user even more. For example in Microsoft Copilot you can use an IPI to switch references, basically giving the user a false answer while showing him that it came from a file they trust.

With people relying more and more on LLMs, even for decision making, the ways an attacker can mess with the info the LLM outputs through the RAG and create a trustworthy forefront present an ever increasing threat

- RAG SECURITY is critical as the main design pattern yet should be broken down into several categories


## AIAssistedSocialEngineering

**Total Votes:** 10

### Justifications:

- AI assisted social engineering (along with phishing attacks) are the first layer of attack through which attackers get into the AI system and its data. By preventing this from happening, most of the follow-up attacks can be prevented. This layer has to be as strong as possible not only for AI-based systems, but for all software systems as well (as experienced in the field).

- should be a new, top-level entry or folded into another larger vulnerability as a concept.

- Social engineering is now personalized and mass-scale. And Cheap. And hard to detect. 

- Social engineering attacks are already dangerous, and using AI attackers can create far more attacks that are increasingly sophisticated. This failure mode has less to do with AI than with existing security systems that will have to deal with both higher quality and quantity because of AI.

- Due to the high success rate of these types of attacks

- This one can be combined with:
PrivacyViolation
SensitiveInformationDisclosure
SupplyChainVulnerabilities
SystemPromptLeakage
UnauthorizedAccessandEntitlementViolations
VoiceModelMisuse - (Due to leaked recording data from a breach)

This is similar to the breach data at #1. But instead of conducting Threat Actor operations, it would be social engineering. With breached data I now have employee information of different departments. I have the necessary customer information to give as responses to any past employee that they may interact with at the target/victim company.  The Threat Actor would also have any past conversations they may have had from saved transcripts to spin a story. All of this can be read off by simple prompts while live, or prepped ahead of time.


## IndirectContextInjection

**Total Votes:** 10

### Justifications:

- Many agents trust all indirect inputs, this attack can bypass guardrails on input prompt making a more dangerous threat

- This attack vector seems to be where many of the traditional malicious approaches could potentially be leveraged.  Many have Blind trust on the completions already.

- Not covered previous and very important - but maybe could be rolled into the prompt injections vuln?

- Should be merged with v2 Candidate #20 Multimodal Injections 


## Overreliancerewrite

**Total Votes:** 8

### Justifications:

- Could be bundled with dangerous hallucinations as it is synergetic to it

- More and more organisations deploy LLMs and increase their reliance on these systems and their accuracy - hence a very important threat

- I think Overreliance is indeed an issue, but not inherent to the LLM itself. Rather, it stems from how it is used. It's a form of Insecure Output Handling, particularly when the downstream system is a human user instead of a cybernetic one. Additionally, 'Developing Insecure Source Code' can be considered a manifestation of Overreliance, as it reflects users' uncritical acceptance of LLM outputs without proper validation.

- Artificial Neural Networks by design need a certain amount of error in their responses otherwise the models can not learn. In ANN terminology we would call that an over-fit model. Therefore, all good models will be wrong at times. 

On the other side of the coin is a model that doesn't fit the data well at all. This could happen for several reasons. 
1) the datasets aren't good enough. 
2) The wrong models are being used. 
3) The models are being misused or poorly designed. 
4) the datasets no longer represent the system they were taken from. (i.e. lets say we had datasets of clothing styles, but the dataset used to train the model was from the 80s.)

I'm not sure this is a security issue for OWASP, but it's going to be a major problem. Even now LLMs will/can give drastically different answers in response to the same question ask to different models.


## ModelInversion

**Total Votes:** 8

### Justifications:

- This could be combined with Model Theft potentially. 

- I think this one might be combined with a few other concepts in the proposed vulns around data disclosure due to prompt-response predictability  

- At least half of the top 10 should be dedicated to protecting the actual behaviour of models - those things that are uniquely AI security and require non-traditional controls.

- Focuses on the threat of reconstructing training data from models, posing significant privacy risks. This is crucial for privacy considerations and could be categorized under "Sensitive Information Disclosure."

- People use all kinds of data to train their models, including data that doesn't fit their values, or may be copyrights, or data that they don't know about. This poses risks to reputation, legal risks, threatens third party privacy, compromises model reliability, and so on. The risk is pervasive and has multiple potential impacts.


## UnauthorizedAccessandEntitlementViolations

**Total Votes:** 8

### Justifications:

- with Rag and other tool chain this is definitely top threat 

- Privilege escalation and access control bypass feel like a co-number 1 in terms of top risks! Ideally LLMs should be out of band from Access Control decisions, but in practice that's super hard.

- Non-AI systems are difficult to manage access to - AI LLM systems are less mature and the environments more complex. 

- very common / required for all / tend to be underestimated importance vs usability


## PrivacyViolation

**Total Votes:** 7

### Justifications:

- should be a new, top-level entry or folded into another larger vulnerability as a concept.

- There is a lot of regulations on privacy, it is key produced outputs are compliant with them.


## AlignmentValueMismatch

**Total Votes:** 6

### Justifications:

- Alignment Value Mismatch is another corner stone with broader future ramifications. Alignment is the key to Gen AI - at any level or at all levels. So need to be at the top level

- This could be a top-level entry, or it could be rolled into Overreliance. This is important to an organization as a whole, so it's important to address to prevent brand/reputation risk. 

- Alignment value mismatch is critical due to its potential ethical implications, operational efficiency concerns, and impacts on trust and acceptance of AI systems. When AI systems diverge from human values or goals, they can make decisions that contradict ethical norms, leading to harm or societal distrust. Ensuring alignment between AI behaviors and human intentions is essential not only for ethical reasons but also for maximizing the effectiveness and acceptance of AI applications. This issue could be considered a top-level entry because it involves fundamental challenges related to ethics, human-AI interaction, and societal impacts. Strategies to address alignment value mismatch include clear specification of human values in AI design, incorporating human oversight in decision-making processes, and continuous evaluation to maintain alignment over time. Whether tackled independently or as part of a broader vulnerability framework, addressing alignment value mismatch is crucial for promoting the ethical deployment and societal acceptance of AI technologies.


## ImproperErrorHandling

**Total Votes:** 5

### Justifications:

- Usually lack of proper error handling is a lack of knowledge about behavior.  We should know the behavior of these models quite well.

- It's obvious to say things should be "designed securely" but improper error handing is easily overlooked and could expose an organization 

- Know your errors and how to handle them


## UIAccessControlManipulation

**Total Votes:** 3

### Justifications:

- Personal data exfiltration from LLM interaction is still a shocking concept to many people - even security professionals expect some privacy here. So we should be careful to make sure UIs are tight and don't leak.


## MultimodelManipulation

**Total Votes:** 2

### Justifications:

- should be a new, top-level entry or folded into another larger vulnerability as a concept.

- Far more dangerous that PI, it will not go through “human eye”


## VoiceModelMisuse

**Total Votes:** 2

### Justifications:

- should be a new, top-level entry or folded into another larger vulnerability as a concept.


## MaliciousLLMTuner

**Total Votes:** 2

### Justifications:

- This deserves own vulnerability. A scan of the LLM for manipulation signs should be available.


## UnrestrictedResourceConsumption

**Total Votes:** 1

### Justifications:

- Unrestricted resource consumption has both virtual and physical world consequences, with poorly maintained and badly misunderstood systems using and abusing energy far beyond our current grid's capacity, worsening living conditions and doing irreparable damage to the environment.

