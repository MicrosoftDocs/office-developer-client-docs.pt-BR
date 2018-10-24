---
title: Seção do arquivo de configuração de formulários [Verbos]
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: e7e1f371-9e9a-4bec-a0b3-87753a16f5e0
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 6a06283e3eb072e1f502d0b1bd303ce9f0733578
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22583971"
---
# <a name="form-configuration-file-verbs-section"></a><span data-ttu-id="34f57-103">Seção do arquivo de configuração de formulários [Verbos]</span><span class="sxs-lookup"><span data-stu-id="34f57-103">Form Configuration File [Verbs] Section</span></span>

  
  
<span data-ttu-id="34f57-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="34f57-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="34f57-105">Seção **[verbos]** lista o conjunto completo de verbos suportados pelo formulário.</span><span class="sxs-lookup"><span data-stu-id="34f57-105">The **[Verbs]** section lists the complete set of verbs supported by the form.</span></span> <span data-ttu-id="34f57-106">O formato da seção **[verbos]** é:</span><span class="sxs-lookup"><span data-stu-id="34f57-106">The format of the **[Verbs]** section is:</span></span> 
  
 <span data-ttu-id="34f57-107">**[Verbos]**</span><span class="sxs-lookup"><span data-stu-id="34f57-107">**[Verbs]**</span></span>
  
 <span data-ttu-id="34f57-108">**Verb1** =  _cadeia de caracteres_</span><span class="sxs-lookup"><span data-stu-id="34f57-108">**Verb1** =  _string_</span></span>
  
<span data-ttu-id="34f57-109">A seguir está um exemplo de uma seção **[verbos]** .</span><span class="sxs-lookup"><span data-stu-id="34f57-109">Following is an example of a **[Verbs]** section.</span></span> 
  
```cpp
[Verbs]
Verb1=1
Verb2=2

```

<span data-ttu-id="34f57-110">Cada verbo é definido em um separado **[verbo.**</span><span class="sxs-lookup"><span data-stu-id="34f57-110">Each verb is defined in a separate **[Verb.**</span></span> <span data-ttu-id="34f57-111">_cadeia de caracteres_ seção **]** .</span><span class="sxs-lookup"><span data-stu-id="34f57-111">_string_ **]** section.</span></span> <span data-ttu-id="34f57-112">Uma **[verbo.**</span><span class="sxs-lookup"><span data-stu-id="34f57-112">A **[Verb.**</span></span> <span data-ttu-id="34f57-113">_cadeia de caracteres_ **]** seção descreve um único verbo oferecido pelo formulário.</span><span class="sxs-lookup"><span data-stu-id="34f57-113">_string_ **]** section describes a single verb offered by the form.</span></span> <span data-ttu-id="34f57-114">A entrada de **DisplayName** em um **[verbo.**</span><span class="sxs-lookup"><span data-stu-id="34f57-114">The **DisplayName** entry in a **[Verb.**</span></span> <span data-ttu-id="34f57-115">_cadeia de caracteres_ seção **]** Especifica o nome do comando exibido na interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="34f57-115">_string_ **]** section specifies the command name displayed in the user interface.</span></span> <span data-ttu-id="34f57-116">A entrada de **código** corresponde ao número verbo passado no método [IMAPIForm::DoVerb](imapiform-doverb.md) .</span><span class="sxs-lookup"><span data-stu-id="34f57-116">The **Code** entry corresponds to the verb number passed in the [IMAPIForm::DoVerb](imapiform-doverb.md) method.</span></span> <span data-ttu-id="34f57-117">A sintaxe para o **[verbo.**</span><span class="sxs-lookup"><span data-stu-id="34f57-117">The syntax for the **[Verb.**</span></span> <span data-ttu-id="34f57-118">_cadeia de caracteres_ seção **]** é:</span><span class="sxs-lookup"><span data-stu-id="34f57-118">_string_ **]** section is:</span></span> 
  
 <span data-ttu-id="34f57-119">**[Verbo.**</span><span class="sxs-lookup"><span data-stu-id="34f57-119">**[Verb.**</span></span> <span data-ttu-id="34f57-120">_cadeia de caracteres_ **]**</span><span class="sxs-lookup"><span data-stu-id="34f57-120">_string_ **]**</span></span>
  
 <span data-ttu-id="34f57-121">**DisplayName** =  _exibido a cadeia de caracteres_</span><span class="sxs-lookup"><span data-stu-id="34f57-121">**DisplayName** =  _displayed string_</span></span>
  
 <span data-ttu-id="34f57-122">**Código** =  _inteiro_</span><span class="sxs-lookup"><span data-stu-id="34f57-122">**Code** =  _integer_</span></span>
  
 <span data-ttu-id="34f57-123">**Sinalizadores** =  _inteiro_</span><span class="sxs-lookup"><span data-stu-id="34f57-123">**Flags** =  _integer_</span></span>
  
 <span data-ttu-id="34f57-124">**Atributos** =  _inteiro_</span><span class="sxs-lookup"><span data-stu-id="34f57-124">**Attribs** =  _integer_</span></span>
  
<span data-ttu-id="34f57-125">A seguir está um exemplo de uma **[verbo.**</span><span class="sxs-lookup"><span data-stu-id="34f57-125">Following is an example of a **[Verb.**</span></span> <span data-ttu-id="34f57-126">_cadeia de caracteres_ seção **]** .</span><span class="sxs-lookup"><span data-stu-id="34f57-126">_string_ **]** section.</span></span> 
  
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

<span data-ttu-id="34f57-127">Verbos listados nesta seção são recuperados por um cliente usando o [método IMAPIFormInfo::CalcVerbSet](imapiforminfo-calcverbset.md).</span><span class="sxs-lookup"><span data-stu-id="34f57-127">Verbs listed in this section are retrieved by a client using the [IMAPIFormInfo::CalcVerbSet method](imapiforminfo-calcverbset.md).</span></span> <span data-ttu-id="34f57-128">Verbos serão ativados chamando o método de [IMAPIForm::DoVerb](imapiform-doverb.md) do formulário e passando-lhe o número de código do verbo a ser executada.</span><span class="sxs-lookup"><span data-stu-id="34f57-128">Verbs are activated by calling the form's [IMAPIForm::DoVerb](imapiform-doverb.md) method and passing it the code number of the verb to be performed.</span></span> 
  

