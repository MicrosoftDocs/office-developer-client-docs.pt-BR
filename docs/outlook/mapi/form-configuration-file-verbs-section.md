---
title: Seção Arquivo de Configuração do Formulário [Verbos]
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: e7e1f371-9e9a-4bec-a0b3-87753a16f5e0
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: bb7d49d69fadab54212ff7e8b50ac969e4890c0a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33417781"
---
# <a name="form-configuration-file-verbs-section"></a><span data-ttu-id="b180b-103">Seção Arquivo de Configuração do Formulário [Verbos]</span><span class="sxs-lookup"><span data-stu-id="b180b-103">Form Configuration File [Verbs] Section</span></span>

  
  
<span data-ttu-id="b180b-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b180b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b180b-105">A **seção [Verbos]** lista o conjunto completo de verbos suportados pelo formulário.</span><span class="sxs-lookup"><span data-stu-id="b180b-105">The **[Verbs]** section lists the complete set of verbs supported by the form.</span></span> <span data-ttu-id="b180b-106">O formato da **seção [Verbos]** é:</span><span class="sxs-lookup"><span data-stu-id="b180b-106">The format of the **[Verbs]** section is:</span></span> 
  
 <span data-ttu-id="b180b-107">**[Verbos]**</span><span class="sxs-lookup"><span data-stu-id="b180b-107">**[Verbs]**</span></span>
  
 <span data-ttu-id="b180b-108">**Verb1**  =   _string_</span><span class="sxs-lookup"><span data-stu-id="b180b-108">**Verb1** =  _string_</span></span>
  
<span data-ttu-id="b180b-109">A seguir está um exemplo de **uma seção [Verbos].**</span><span class="sxs-lookup"><span data-stu-id="b180b-109">Following is an example of a **[Verbs]** section.</span></span> 
  
```cpp
[Verbs]
Verb1=1
Verb2=2

```

<span data-ttu-id="b180b-110">Cada verbo é definido em um **[Verbo] separado.**</span><span class="sxs-lookup"><span data-stu-id="b180b-110">Each verb is defined in a separate **[Verb.**</span></span> <span data-ttu-id="b180b-111">_seção string_ **]** .</span><span class="sxs-lookup"><span data-stu-id="b180b-111">_string_ **]** section.</span></span> <span data-ttu-id="b180b-112">A **[Verbo.**</span><span class="sxs-lookup"><span data-stu-id="b180b-112">A **[Verb.**</span></span> <span data-ttu-id="b180b-113">_string_ **]** section describes a single verb offered by the form.</span><span class="sxs-lookup"><span data-stu-id="b180b-113">_string_ **]** section describes a single verb offered by the form.</span></span> <span data-ttu-id="b180b-114">A **entrada DisplayName** em um **[Verbo.**</span><span class="sxs-lookup"><span data-stu-id="b180b-114">The **DisplayName** entry in a **[Verb.**</span></span> <span data-ttu-id="b180b-115">_string_ **]** section specifies the command name displayed in the user interface.</span><span class="sxs-lookup"><span data-stu-id="b180b-115">_string_ **]** section specifies the command name displayed in the user interface.</span></span> <span data-ttu-id="b180b-116">A **entrada** de código corresponde ao número do verbo passado no [método IMAPIForm::D oVerb.](imapiform-doverb.md)</span><span class="sxs-lookup"><span data-stu-id="b180b-116">The **Code** entry corresponds to the verb number passed in the [IMAPIForm::DoVerb](imapiform-doverb.md) method.</span></span> <span data-ttu-id="b180b-117">A sintaxe do **[Verbo.**</span><span class="sxs-lookup"><span data-stu-id="b180b-117">The syntax for the **[Verb.**</span></span> <span data-ttu-id="b180b-118">_string_ **]** section is:</span><span class="sxs-lookup"><span data-stu-id="b180b-118">_string_ **]** section is:</span></span> 
  
 <span data-ttu-id="b180b-119">**[Verbo.**</span><span class="sxs-lookup"><span data-stu-id="b180b-119">**[Verb.**</span></span> <span data-ttu-id="b180b-120">_string_ **]**</span><span class="sxs-lookup"><span data-stu-id="b180b-120">_string_ **]**</span></span>
  
 <span data-ttu-id="b180b-121">**DisplayName**  =   _cadeia de caracteres exibida_</span><span class="sxs-lookup"><span data-stu-id="b180b-121">**DisplayName** =  _displayed string_</span></span>
  
 <span data-ttu-id="b180b-122">**Código**  =   _integer_</span><span class="sxs-lookup"><span data-stu-id="b180b-122">**Code** =  _integer_</span></span>
  
 <span data-ttu-id="b180b-123">**Sinalizadores**  =   _integer_</span><span class="sxs-lookup"><span data-stu-id="b180b-123">**Flags** =  _integer_</span></span>
  
 <span data-ttu-id="b180b-124">**Atribs**  =   _integer_</span><span class="sxs-lookup"><span data-stu-id="b180b-124">**Attribs** =  _integer_</span></span>
  
<span data-ttu-id="b180b-125">A seguir está um exemplo de **um [Verbo.**</span><span class="sxs-lookup"><span data-stu-id="b180b-125">Following is an example of a **[Verb.**</span></span> <span data-ttu-id="b180b-126">_seção string_ **]** .</span><span class="sxs-lookup"><span data-stu-id="b180b-126">_string_ **]** section.</span></span> 
  
```cpp
[Verb.1]
DisplayName=Reply
code=1
Flags=0
Attribs=2
[Verb.2]
DisplayName=Delete
Code=2
Flags=0
Attribs=2

```

<span data-ttu-id="b180b-127">Os verbos listados nesta seção são recuperados por um cliente usando o [método IMAPIFormInfo::CalcVerbSet](imapiforminfo-calcverbset.md).</span><span class="sxs-lookup"><span data-stu-id="b180b-127">Verbs listed in this section are retrieved by a client using the [IMAPIFormInfo::CalcVerbSet method](imapiforminfo-calcverbset.md).</span></span> <span data-ttu-id="b180b-128">Os verbos são ativados chamando o método [IMAPIForm::D oVerb](imapiform-doverb.md) do formulário e passando a ele o número de código do verbo a ser executado.</span><span class="sxs-lookup"><span data-stu-id="b180b-128">Verbs are activated by calling the form's [IMAPIForm::DoVerb](imapiform-doverb.md) method and passing it the code number of the verb to be performed.</span></span> 
  

