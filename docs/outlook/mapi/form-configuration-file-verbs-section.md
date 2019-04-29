---
title: Seção do arquivo de configuração de formulários [verbos]
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
# <a name="form-configuration-file-verbs-section"></a><span data-ttu-id="faeb0-103">Seção do arquivo de configuração de formulários [verbos]</span><span class="sxs-lookup"><span data-stu-id="faeb0-103">Form Configuration File [Verbs] Section</span></span>

  
  
<span data-ttu-id="faeb0-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="faeb0-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="faeb0-105">A seção **[verbos]** lista o conjunto completo de verbos com suporte no formulário.</span><span class="sxs-lookup"><span data-stu-id="faeb0-105">The **[Verbs]** section lists the complete set of verbs supported by the form.</span></span> <span data-ttu-id="faeb0-106">O formato da seção **[verbos]** é:</span><span class="sxs-lookup"><span data-stu-id="faeb0-106">The format of the **[Verbs]** section is:</span></span> 
  
 <span data-ttu-id="faeb0-107">**Verbos**</span><span class="sxs-lookup"><span data-stu-id="faeb0-107">**[Verbs]**</span></span>
  
 <span data-ttu-id="faeb0-108">\*\*\*\* =  _Cadeia de caracteres_ Verb1</span><span class="sxs-lookup"><span data-stu-id="faeb0-108">**Verb1** =  _string_</span></span>
  
<span data-ttu-id="faeb0-109">Veja a seguir um exemplo de uma seção de **[verbos]** .</span><span class="sxs-lookup"><span data-stu-id="faeb0-109">Following is an example of a **[Verbs]** section.</span></span> 
  
```cpp
[Verbs]
Verb1=1
Verb2=2

```

<span data-ttu-id="faeb0-110">Cada verbo é definido em um **[verbo separado.**</span><span class="sxs-lookup"><span data-stu-id="faeb0-110">Each verb is defined in a separate **[Verb.**</span></span> <span data-ttu-id="faeb0-111">_cadeia de caracteres_ **]** seção.</span><span class="sxs-lookup"><span data-stu-id="faeb0-111">_string_ **]** section.</span></span> <span data-ttu-id="faeb0-112">Um **[verbo.**</span><span class="sxs-lookup"><span data-stu-id="faeb0-112">A **[Verb.**</span></span> <span data-ttu-id="faeb0-113">_cadeia de caracteres_ **]** descreve um único verbo oferecido pelo formulário.</span><span class="sxs-lookup"><span data-stu-id="faeb0-113">_string_ **]** section describes a single verb offered by the form.</span></span> <span data-ttu-id="faeb0-114">A entrada **DisplayName** em um **[Verb.**</span><span class="sxs-lookup"><span data-stu-id="faeb0-114">The **DisplayName** entry in a **[Verb.**</span></span> <span data-ttu-id="faeb0-115">_cadeia de caracteres_ **]** seção especifica o nome do comando exibido na interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="faeb0-115">_string_ **]** section specifies the command name displayed in the user interface.</span></span> <span data-ttu-id="faeb0-116">A entrada de **código** corresponde ao número de verbo passado no método [IMAPIForm::D overb](imapiform-doverb.md) .</span><span class="sxs-lookup"><span data-stu-id="faeb0-116">The **Code** entry corresponds to the verb number passed in the [IMAPIForm::DoVerb](imapiform-doverb.md) method.</span></span> <span data-ttu-id="faeb0-117">A sintaxe do **verbo [.**</span><span class="sxs-lookup"><span data-stu-id="faeb0-117">The syntax for the **[Verb.**</span></span> <span data-ttu-id="faeb0-118">_cadeia de caracteres_ **]** seção é:</span><span class="sxs-lookup"><span data-stu-id="faeb0-118">_string_ **]** section is:</span></span> 
  
 <span data-ttu-id="faeb0-119">**Verbo.**</span><span class="sxs-lookup"><span data-stu-id="faeb0-119">**[Verb.**</span></span> <span data-ttu-id="faeb0-120">_cadeia de caracteres_ **]**</span><span class="sxs-lookup"><span data-stu-id="faeb0-120">_string_ **]**</span></span>
  
 <span data-ttu-id="faeb0-121">\*\*\*\* =  _Cadeia de caracteres exibida_ DisplayName</span><span class="sxs-lookup"><span data-stu-id="faeb0-121">**DisplayName** =  _displayed string_</span></span>
  
 <span data-ttu-id="faeb0-122">\*\*\*\* =  _Inteiro_ de código</span><span class="sxs-lookup"><span data-stu-id="faeb0-122">**Code** =  _integer_</span></span>
  
 <span data-ttu-id="faeb0-123">\*\*\*\* =  _Inteiro_ de sinalizadores</span><span class="sxs-lookup"><span data-stu-id="faeb0-123">**Flags** =  _integer_</span></span>
  
 <span data-ttu-id="faeb0-124">\*\*\*\* Número inteiro de attrib__  =  </span><span class="sxs-lookup"><span data-stu-id="faeb0-124">**Attribs** =  _integer_</span></span>
  
<span data-ttu-id="faeb0-125">Veja a seguir um exemplo de um **verbo [.**</span><span class="sxs-lookup"><span data-stu-id="faeb0-125">Following is an example of a **[Verb.**</span></span> <span data-ttu-id="faeb0-126">_cadeia de caracteres_ **]** seção.</span><span class="sxs-lookup"><span data-stu-id="faeb0-126">_string_ **]** section.</span></span> 
  
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

<span data-ttu-id="faeb0-127">Os verbos listados nesta seção são recuperados por um cliente usando o [método IMAPIFormInfo:: CalcVerbSet](imapiforminfo-calcverbset.md).</span><span class="sxs-lookup"><span data-stu-id="faeb0-127">Verbs listed in this section are retrieved by a client using the [IMAPIFormInfo::CalcVerbSet method](imapiforminfo-calcverbset.md).</span></span> <span data-ttu-id="faeb0-128">Os verbos são ativados chamando o método [IMAPIForm::D overb](imapiform-doverb.md) do formulário e passando-o número de código do verbo a ser executado.</span><span class="sxs-lookup"><span data-stu-id="faeb0-128">Verbs are activated by calling the form's [IMAPIForm::DoVerb](imapiform-doverb.md) method and passing it the code number of the verb to be performed.</span></span> 
  

