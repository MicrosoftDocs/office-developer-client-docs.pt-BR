---
title: Seção Arquivo de Configuração de Formulário [Extensões]
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 4817e446-982d-491c-abcf-cc888a771afa
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 96682dd2bdfedc42ea13c6985cb834f0adffd4df
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33423752"
---
# <a name="form-configuration-file-extensions-section"></a><span data-ttu-id="0f42a-103">Seção Arquivo de Configuração de Formulário [Extensões]</span><span class="sxs-lookup"><span data-stu-id="0f42a-103">Form Configuration File [Extensions] Section</span></span>

  
  
<span data-ttu-id="0f42a-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="0f42a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="0f42a-105">A seção **[Extensões]** lista os atributos estendidos do formulário, normalmente um conjunto de propriedades nomeados, que são quaisquer atributos além dos básicos listados na seção **[Descrição]** do arquivo de configuração do formulário.</span><span class="sxs-lookup"><span data-stu-id="0f42a-105">The **[Extensions]** section lists the extended attributes of the form, typically a named property set, which are any attributes beyond the basic ones listed in the **[Description]** section of the form configuration file.</span></span> <span data-ttu-id="0f42a-106">Atributos estendidos são propriedades retornadas de chamadas para o método **GetProps** do objeto **IMAPIFormInfo** com o bit alto definido na marca de propriedade.</span><span class="sxs-lookup"><span data-stu-id="0f42a-106">Extended attributes are properties returned from calls to the **GetProps** method of the **IMAPIFormInfo** object with the high bit set in the property tag.</span></span> <span data-ttu-id="0f42a-107">Os aplicativos cliente podem determinar os atributos estendidos de um formulário, se necessário, recuperando essas marcas.</span><span class="sxs-lookup"><span data-stu-id="0f42a-107">Client applications can determine a form's extended attributes, if any, by retrieving these tags.</span></span> <span data-ttu-id="0f42a-108">Para fazer isso, os clientes chamam o método [IMAPIProp::GetIDsFromNames,](imapiprop-getidsfromnames.md) passando os nomes das propriedades do formulário e chamam o método [IMAPIProp::GetProps](imapiprop-getprops.md) para obter as propriedades.</span><span class="sxs-lookup"><span data-stu-id="0f42a-108">To do so, clients call the [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) method, passing in the names of the form's properties and call the [IMAPIProp::GetProps](imapiprop-getprops.md) method to get the properties.</span></span> 
  
 <span data-ttu-id="0f42a-109">**[Extensões]**</span><span class="sxs-lookup"><span data-stu-id="0f42a-109">**[Extensions]**</span></span>
  
 <span data-ttu-id="0f42a-110">**Extensão.**</span><span class="sxs-lookup"><span data-stu-id="0f42a-110">**Extension.**</span></span> <span data-ttu-id="0f42a-111">_string1_  =   _string2_</span><span class="sxs-lookup"><span data-stu-id="0f42a-111">_string1_ =  _string2_</span></span>
  
<span data-ttu-id="0f42a-112">Cada seção de propriedade de extensão define um atributo de extensão usando a sintaxe de propriedade nomeada MAPI.</span><span class="sxs-lookup"><span data-stu-id="0f42a-112">Each extension property section defines one extension attribute using the MAPI named property syntax.</span></span> <span data-ttu-id="0f42a-113">O tipo de propriedade deve ser PT_LONG ou PT_STRING8.</span><span class="sxs-lookup"><span data-stu-id="0f42a-113">The property type must be either PT_LONG or PT_STRING8.</span></span> <span data-ttu-id="0f42a-114">Não há suporte para conjuntos de propriedades que contenham cadeias de caracteres nomeadas.</span><span class="sxs-lookup"><span data-stu-id="0f42a-114">Property sets that contains named strings are not supported.</span></span> <span data-ttu-id="0f42a-115">O formato da **seção [Extensão]** é:</span><span class="sxs-lookup"><span data-stu-id="0f42a-115">The format of the **[Extension]** section is:</span></span> 
  
 <span data-ttu-id="0f42a-116">**[Extensão.**</span><span class="sxs-lookup"><span data-stu-id="0f42a-116">**[Extension.**</span></span> <span data-ttu-id="0f42a-117">_string2_ **]**</span><span class="sxs-lookup"><span data-stu-id="0f42a-117">_string2_ **]**</span></span>
  
 <span data-ttu-id="0f42a-118">**Tipo**  =   _integer_</span><span class="sxs-lookup"><span data-stu-id="0f42a-118">**Type** =  _integer_</span></span>
  
 <span data-ttu-id="0f42a-119">**NmidPropset**  =   _guid_</span><span class="sxs-lookup"><span data-stu-id="0f42a-119">**NmidPropset** =  _guid_</span></span>
  
 <span data-ttu-id="0f42a-120">**NmidInteger**  =   _integer_</span><span class="sxs-lookup"><span data-stu-id="0f42a-120">**NmidInteger** =  _integer_</span></span>
  
 <span data-ttu-id="0f42a-121">**Valor**  =   _string_  |   _integer_</span><span class="sxs-lookup"><span data-stu-id="0f42a-121">**Value** =  _string_ |  _integer_</span></span>
  
<span data-ttu-id="0f42a-122">Um exemplo de uma **seção [Extensões]** e uma seção relacionada subsequente é mostrado a seguir.</span><span class="sxs-lookup"><span data-stu-id="0f42a-122">An example of an **[Extensions]** section and a subsequent related section is shown following.</span></span> 
  
```
[Extensions]
Extension.A = 1
[Extension.1]
Type = 30
NmidPropset = {00020D0C-0000-0000-C000-000000000046}
NmidInteger = 1
Value = 11220000

```


