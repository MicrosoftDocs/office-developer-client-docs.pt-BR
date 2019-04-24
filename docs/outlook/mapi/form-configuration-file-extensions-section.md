---
title: Seção do arquivo de configuração de formulários [extensões]
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 4817e446-982d-491c-abcf-cc888a771afa
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 96682dd2bdfedc42ea13c6985cb834f0adffd4df
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32327297"
---
# <a name="form-configuration-file-extensions-section"></a><span data-ttu-id="ad151-103">Seção do arquivo de configuração de formulários [extensões]</span><span class="sxs-lookup"><span data-stu-id="ad151-103">Form Configuration File [Extensions] Section</span></span>

  
  
<span data-ttu-id="ad151-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ad151-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ad151-105">A seção **[Extensions]** lista os atributos estendidos do formulário, geralmente um conjunto de propriedades nomeadas, que são qualquer atributo além dos básicos listados na seção **[Description]** do arquivo de configuração de formulário.</span><span class="sxs-lookup"><span data-stu-id="ad151-105">The **[Extensions]** section lists the extended attributes of the form, typically a named property set, which are any attributes beyond the basic ones listed in the **[Description]** section of the form configuration file.</span></span> <span data-ttu-id="ad151-106">Os atributos estendidos são propriedades retornadas de \*\*\*\* chamadas para o método GetProps do objeto **IMAPIFormInfo** com o bit alto definido na marca da propriedade.</span><span class="sxs-lookup"><span data-stu-id="ad151-106">Extended attributes are properties returned from calls to the **GetProps** method of the **IMAPIFormInfo** object with the high bit set in the property tag.</span></span> <span data-ttu-id="ad151-107">Os aplicativos cliente podem determinar os atributos estendidos de um formulário, se houver, recuperando essas marcas.</span><span class="sxs-lookup"><span data-stu-id="ad151-107">Client applications can determine a form's extended attributes, if any, by retrieving these tags.</span></span> <span data-ttu-id="ad151-108">Para fazer isso, os clientes chamam o método [IMAPIProp:: GetIDsFromNames](imapiprop-getidsfromnames.md) , passando os nomes das propriedades do formulário e chamar o método [IMAPIProp::](imapiprop-getprops.md) GetProps para obter as propriedades.</span><span class="sxs-lookup"><span data-stu-id="ad151-108">To do so, clients call the [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) method, passing in the names of the form's properties and call the [IMAPIProp::GetProps](imapiprop-getprops.md) method to get the properties.</span></span> 
  
 <span data-ttu-id="ad151-109">**Das**</span><span class="sxs-lookup"><span data-stu-id="ad151-109">**[Extensions]**</span></span>
  
 <span data-ttu-id="ad151-110">**Extensões.**</span><span class="sxs-lookup"><span data-stu-id="ad151-110">**Extension.**</span></span> <span data-ttu-id="ad151-111">_seqüência1_ =  _seqüência2_</span><span class="sxs-lookup"><span data-stu-id="ad151-111">_string1_ =  _string2_</span></span>
  
<span data-ttu-id="ad151-112">Cada seção de propriedades de extensão define um atributo de extensão usando a sintaxe da propriedade nomeada MAPI.</span><span class="sxs-lookup"><span data-stu-id="ad151-112">Each extension property section defines one extension attribute using the MAPI named property syntax.</span></span> <span data-ttu-id="ad151-113">O tipo de propriedade deve ser PT_LONG ou PT_STRING8.</span><span class="sxs-lookup"><span data-stu-id="ad151-113">The property type must be either PT_LONG or PT_STRING8.</span></span> <span data-ttu-id="ad151-114">Não há suporte para conjuntos de propriedades que contenham cadeias de caracteres nomeadas.</span><span class="sxs-lookup"><span data-stu-id="ad151-114">Property sets that contains named strings are not supported.</span></span> <span data-ttu-id="ad151-115">O formato da seção **[Extension]** é:</span><span class="sxs-lookup"><span data-stu-id="ad151-115">The format of the **[Extension]** section is:</span></span> 
  
 <span data-ttu-id="ad151-116">**Extensões.**</span><span class="sxs-lookup"><span data-stu-id="ad151-116">**[Extension.**</span></span> <span data-ttu-id="ad151-117">_seqüência2_ **]**</span><span class="sxs-lookup"><span data-stu-id="ad151-117">_string2_ **]**</span></span>
  
 <span data-ttu-id="ad151-118">**Tipo** =  _inteiro_</span><span class="sxs-lookup"><span data-stu-id="ad151-118">**Type** =  _integer_</span></span>
  
 <span data-ttu-id="ad151-119">\*\*\*\* =  _GUID_ NmidPropset</span><span class="sxs-lookup"><span data-stu-id="ad151-119">**NmidPropset** =  _guid_</span></span>
  
 <span data-ttu-id="ad151-120">**NmidInteger** =  _inteiro_</span><span class="sxs-lookup"><span data-stu-id="ad151-120">**NmidInteger** =  _integer_</span></span>
  
 <span data-ttu-id="ad151-121">**Valor** =  __ |  _inteiro_ da cadeia de caracteres</span><span class="sxs-lookup"><span data-stu-id="ad151-121">**Value** =  _string_ |  _integer_</span></span>
  
<span data-ttu-id="ad151-122">Um exemplo de uma seção **[Extensions]** e uma seção relacionada subsequentes são mostrados a seguir.</span><span class="sxs-lookup"><span data-stu-id="ad151-122">An example of an **[Extensions]** section and a subsequent related section is shown following.</span></span> 
  
```
[Extensions]
Extension.A = 1
[Extension.1]
Type = 30
NmidPropset = {00020D0C-0000-0000-C000-000000000046}
NmidInteger = 1
Value = 11220000

```


