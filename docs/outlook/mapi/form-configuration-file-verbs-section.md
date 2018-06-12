---
title: Seção de [verbos] do arquivo de configuração de formulário
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: e7e1f371-9e9a-4bec-a0b3-87753a16f5e0
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 5fe1b064b48bc9112a872677fbf5042b7dfe5449
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19766589"
---
# <a name="form-configuration-file-verbs-section"></a><span data-ttu-id="b731c-103">Seção de [verbos] do arquivo de configuração de formulário</span><span class="sxs-lookup"><span data-stu-id="b731c-103">Form Configuration File [Verbs] Section</span></span>

  
  
<span data-ttu-id="b731c-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="b731c-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="b731c-105">Seção **[verbos]** lista o conjunto completo de verbos suportados pelo formulário.</span><span class="sxs-lookup"><span data-stu-id="b731c-105">The **[Verbs]** section lists the complete set of verbs supported by the form.</span></span> <span data-ttu-id="b731c-106">O formato da seção **[verbos]** é:</span><span class="sxs-lookup"><span data-stu-id="b731c-106">The format of the **[Verbs]** section is:</span></span> 
  
 <span data-ttu-id="b731c-107">**[Verbos]**</span><span class="sxs-lookup"><span data-stu-id="b731c-107">**[Verbs]**</span></span>
  
 <span data-ttu-id="b731c-108">**Verb1** =  _cadeia de caracteres_</span><span class="sxs-lookup"><span data-stu-id="b731c-108">**Verb1** =  _string_</span></span>
  
<span data-ttu-id="b731c-109">A seguir está um exemplo de uma seção **[verbos]** .</span><span class="sxs-lookup"><span data-stu-id="b731c-109">Following is an example of a **[Verbs]** section.</span></span> 
  
```cpp
[Verbs]
Verb1=1
Verb2=2

```

<span data-ttu-id="b731c-110">Cada verbo é definido em um separado **[verbo.**</span><span class="sxs-lookup"><span data-stu-id="b731c-110">Each verb is defined in a separate **[Verb.**</span></span> <span data-ttu-id="b731c-111">_cadeia de caracteres_ seção **]** .</span><span class="sxs-lookup"><span data-stu-id="b731c-111">_string_ **]** section.</span></span> <span data-ttu-id="b731c-112">Uma **[verbo.**</span><span class="sxs-lookup"><span data-stu-id="b731c-112">A **[Verb.**</span></span> <span data-ttu-id="b731c-113">_cadeia de caracteres_ **]** seção descreve um único verbo oferecido pelo formulário.</span><span class="sxs-lookup"><span data-stu-id="b731c-113">_string_ **]** section describes a single verb offered by the form.</span></span> <span data-ttu-id="b731c-114">A entrada de **DisplayName** em um **[verbo.**</span><span class="sxs-lookup"><span data-stu-id="b731c-114">The **DisplayName** entry in a **[Verb.**</span></span> <span data-ttu-id="b731c-115">_cadeia de caracteres_ seção **]** Especifica o nome do comando exibido na interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="b731c-115">_string_ **]** section specifies the command name displayed in the user interface.</span></span> <span data-ttu-id="b731c-116">A entrada de **código** corresponde ao número verbo passado no método [IMAPIForm::DoVerb](imapiform-doverb.md) .</span><span class="sxs-lookup"><span data-stu-id="b731c-116">The **Code** entry corresponds to the verb number passed in the [IMAPIForm::DoVerb](imapiform-doverb.md) method.</span></span> <span data-ttu-id="b731c-117">A sintaxe para o **[verbo.**</span><span class="sxs-lookup"><span data-stu-id="b731c-117">The syntax for the **[Verb.**</span></span> <span data-ttu-id="b731c-118">_cadeia de caracteres_ seção **]** é:</span><span class="sxs-lookup"><span data-stu-id="b731c-118">_string_ **]** section is:</span></span> 
  
 <span data-ttu-id="b731c-119">**[Verbo.**</span><span class="sxs-lookup"><span data-stu-id="b731c-119">**[Verb.**</span></span> <span data-ttu-id="b731c-120">_cadeia de caracteres_ **]**</span><span class="sxs-lookup"><span data-stu-id="b731c-120">_string_ **]**</span></span>
  
 <span data-ttu-id="b731c-121">**DisplayName** =  _exibido a cadeia de caracteres_</span><span class="sxs-lookup"><span data-stu-id="b731c-121">**DisplayName** =  _displayed string_</span></span>
  
 <span data-ttu-id="b731c-122">**Código** =  _inteiro_</span><span class="sxs-lookup"><span data-stu-id="b731c-122">**Code** =  _integer_</span></span>
  
 <span data-ttu-id="b731c-123">**Sinalizadores** =  _inteiro_</span><span class="sxs-lookup"><span data-stu-id="b731c-123">**Flags** =  _integer_</span></span>
  
 <span data-ttu-id="b731c-124">**Atributos** =  _inteiro_</span><span class="sxs-lookup"><span data-stu-id="b731c-124">**Attribs** =  _integer_</span></span>
  
<span data-ttu-id="b731c-125">A seguir está um exemplo de uma **[verbo.**</span><span class="sxs-lookup"><span data-stu-id="b731c-125">Following is an example of a **[Verb.**</span></span> <span data-ttu-id="b731c-126">_cadeia de caracteres_ seção **]** .</span><span class="sxs-lookup"><span data-stu-id="b731c-126">_string_ **]** section.</span></span> 
  
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

<span data-ttu-id="b731c-127">Verbos listados nesta seção são recuperados por um cliente usando o [método IMAPIFormInfo::CalcVerbSet](imapiforminfo-calcverbset.md).</span><span class="sxs-lookup"><span data-stu-id="b731c-127">Verbs listed in this section are retrieved by a client using the [IMAPIFormInfo::CalcVerbSet method](imapiforminfo-calcverbset.md).</span></span> <span data-ttu-id="b731c-128">Verbos serão ativados chamando o método de [IMAPIForm::DoVerb](imapiform-doverb.md) do formulário e passando-lhe o número de código do verbo a ser executada.</span><span class="sxs-lookup"><span data-stu-id="b731c-128">Verbs are activated by calling the form's [IMAPIForm::DoVerb](imapiform-doverb.md) method and passing it the code number of the verb to be performed.</span></span> 
  

