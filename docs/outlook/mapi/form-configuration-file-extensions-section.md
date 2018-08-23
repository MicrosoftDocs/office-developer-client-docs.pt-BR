---
title: Seção do arquivo de configuração de formulários [Extensões]
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 4817e446-982d-491c-abcf-cc888a771afa
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 459c5f5a34421583141028cd9accad5e242d31ad
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22573555"
---
# <a name="form-configuration-file-extensions-section"></a><span data-ttu-id="7dfdc-103">Seção do arquivo de configuração de formulários [Extensões]</span><span class="sxs-lookup"><span data-stu-id="7dfdc-103">Form Configuration File [Extensions] Section</span></span>

  
  
<span data-ttu-id="7dfdc-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7dfdc-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7dfdc-105">A seção **[Extensions]** lista os atributos estendidos do formulário, geralmente um conjunto nomeado de propriedade, que são atributos além dos básicos listados na seção **[descrição]** do arquivo de configuração de formulário.</span><span class="sxs-lookup"><span data-stu-id="7dfdc-105">The **[Extensions]** section lists the extended attributes of the form, typically a named property set, which are any attributes beyond the basic ones listed in the **[Description]** section of the form configuration file.</span></span> <span data-ttu-id="7dfdc-106">Os atributos estendidos são retornadas de chamadas para o método **GetProps** do objeto **IMAPIFormInfo** com alto definido o bit definido na marca de propriedade de propriedades.</span><span class="sxs-lookup"><span data-stu-id="7dfdc-106">Extended attributes are properties returned from calls to the **GetProps** method of the **IMAPIFormInfo** object with the high bit set in the property tag.</span></span> <span data-ttu-id="7dfdc-107">Aplicativos cliente podem determinar os atributos estendidos de um formulário, se houver, recuperando essas marcas.</span><span class="sxs-lookup"><span data-stu-id="7dfdc-107">Client applications can determine a form's extended attributes, if any, by retrieving these tags.</span></span> <span data-ttu-id="7dfdc-108">Para fazer isso, os clientes chamar o método [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) , passando nos nomes de propriedades do formulário e chame o método [IMAPIProp::GetProps](imapiprop-getprops.md) para obter as propriedades.</span><span class="sxs-lookup"><span data-stu-id="7dfdc-108">To do so, clients call the [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) method, passing in the names of the form's properties and call the [IMAPIProp::GetProps](imapiprop-getprops.md) method to get the properties.</span></span> 
  
 <span data-ttu-id="7dfdc-109">**[Extensions]**</span><span class="sxs-lookup"><span data-stu-id="7dfdc-109">**[Extensions]**</span></span>
  
 <span data-ttu-id="7dfdc-110">**Extensão.**</span><span class="sxs-lookup"><span data-stu-id="7dfdc-110">**Extension.**</span></span> <span data-ttu-id="7dfdc-111">_sequência1_ =  _sequência2_</span><span class="sxs-lookup"><span data-stu-id="7dfdc-111">_string1_ =  _string2_</span></span>
  
<span data-ttu-id="7dfdc-112">Cada seção de propriedade de extensão define um atributo de extensão usando MAPI denominada a sintaxe da propriedade.</span><span class="sxs-lookup"><span data-stu-id="7dfdc-112">Each extension property section defines one extension attribute using the MAPI named property syntax.</span></span> <span data-ttu-id="7dfdc-113">O tipo de propriedade deve ser PT_LONG ou PT_STRING8.</span><span class="sxs-lookup"><span data-stu-id="7dfdc-113">The property type must be either PT_LONG or PT_STRING8.</span></span> <span data-ttu-id="7dfdc-114">Conjuntos de propriedades que contém as cadeias de caracteres nomeadas não são suportados.</span><span class="sxs-lookup"><span data-stu-id="7dfdc-114">Property sets that contains named strings are not supported.</span></span> <span data-ttu-id="7dfdc-115">O formato da seção **[extensão]** é:</span><span class="sxs-lookup"><span data-stu-id="7dfdc-115">The format of the **[Extension]** section is:</span></span> 
  
 <span data-ttu-id="7dfdc-116">**[Extensão.**</span><span class="sxs-lookup"><span data-stu-id="7dfdc-116">**[Extension.**</span></span> <span data-ttu-id="7dfdc-117">_Sequência2_ **]**</span><span class="sxs-lookup"><span data-stu-id="7dfdc-117">_string2_ **]**</span></span>
  
 <span data-ttu-id="7dfdc-118">**Tipo** =  _inteiro_</span><span class="sxs-lookup"><span data-stu-id="7dfdc-118">**Type** =  _integer_</span></span>
  
 <span data-ttu-id="7dfdc-119">**NmidPropset** =  _guid_</span><span class="sxs-lookup"><span data-stu-id="7dfdc-119">**NmidPropset** =  _guid_</span></span>
  
 <span data-ttu-id="7dfdc-120">**Opção NmidInteger** =  _inteiro_</span><span class="sxs-lookup"><span data-stu-id="7dfdc-120">**NmidInteger** =  _integer_</span></span>
  
 <span data-ttu-id="7dfdc-121">**Valor** =  _cadeia de caracteres_ |  _inteiro_</span><span class="sxs-lookup"><span data-stu-id="7dfdc-121">**Value** =  _string_ |  _integer_</span></span>
  
<span data-ttu-id="7dfdc-122">Um exemplo de uma seção **[Extensions]** e uma seção relacionada subsequente é mostrado a seguir.</span><span class="sxs-lookup"><span data-stu-id="7dfdc-122">An example of an **[Extensions]** section and a subsequent related section is shown following.</span></span> 
  
```
[Extensions]
Extension.A = 1
[Extension.1]
Type = 30
NmidPropset = {00020D0C-0000-0000-C000-000000000046}
NmidInteger = 1
Value = 11220000

```


