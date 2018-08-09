---
title: Função FONT
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 20b587ee-87bf-4648-99ec-ddedd703d9fd
description: Retorna o valor inteiro do identificador exclusivo para uma fonte, especificada por nome.
ms.openlocfilehash: 4afd2aa05f2103675bf0df8db5cc7ea21f45fe71
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19771919"
---
# <a name="font-function"></a><span data-ttu-id="94fe3-103">Função FONT</span><span class="sxs-lookup"><span data-stu-id="94fe3-103">FONT Function</span></span>

<span data-ttu-id="94fe3-104">Retorna o valor inteiro do identificador exclusivo para uma fonte, especificada por nome.</span><span class="sxs-lookup"><span data-stu-id="94fe3-104">Returns the integer value of the unique identifier for a font, specified by name.</span></span>
  
> [!NOTE]
> <span data-ttu-id="94fe3-105">Na maioria dos casos, o identificador de fonte é específica ao sistema.</span><span class="sxs-lookup"><span data-stu-id="94fe3-105">In most cases, the font identifier is system-specific.</span></span> <span data-ttu-id="94fe3-106">Embora a fonte permanece estabelecida uma vez usado em um arquivo, a função de **fonte** fornece acesso consistente para uma fonte específica entre sistemas e versões do Visio.</span><span class="sxs-lookup"><span data-stu-id="94fe3-106">Although the font remains established once used in a file, the **FONT** function provides consistent access to a particular font across systems and versions of Visio.</span></span> <span data-ttu-id="94fe3-107">É recomendável que você use a função de **fonte** para atribuir fontes em vez de referir-se diretamente aos identificadores de fonte.</span><span class="sxs-lookup"><span data-stu-id="94fe3-107">It is recommended that you use the **FONT** function to assign fonts instead of referring to font identifiers directly.</span></span> 
  
## <a name="version-information"></a><span data-ttu-id="94fe3-108">Informações da versão</span><span class="sxs-lookup"><span data-stu-id="94fe3-108">Version Information</span></span>

<span data-ttu-id="94fe3-109">Version Added: Visio 2013
</span><span class="sxs-lookup"><span data-stu-id="94fe3-109">Version Added: Visio 2013</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="94fe3-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="94fe3-110">Syntax</span></span>

 <span data-ttu-id="94fe3-111">**Fonte** ( _"font_name_string"_)</span><span class="sxs-lookup"><span data-stu-id="94fe3-111">**FONT**( _"font_name_string"_)</span></span>
  
### <a name="parameters"></a><span data-ttu-id="94fe3-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="94fe3-112">Parameters</span></span>

|<span data-ttu-id="94fe3-113">**Name**</span><span class="sxs-lookup"><span data-stu-id="94fe3-113">**Name**</span></span>|<span data-ttu-id="94fe3-114">**Obrigatório/Opcional**</span><span class="sxs-lookup"><span data-stu-id="94fe3-114">**Required/Optional**</span></span>|<span data-ttu-id="94fe3-115">**Tipo de dados**</span><span class="sxs-lookup"><span data-stu-id="94fe3-115">**Data Type**</span></span>|<span data-ttu-id="94fe3-116">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="94fe3-116">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="94fe3-117">_font_name_string_</span><span class="sxs-lookup"><span data-stu-id="94fe3-117">_font_name_string_</span></span> <br/> |<span data-ttu-id="94fe3-118">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="94fe3-118">Required</span></span>  <br/> |<span data-ttu-id="94fe3-119">**cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="94fe3-119">**string**</span></span> <br/> |<span data-ttu-id="94fe3-120">O nome da fonte.</span><span class="sxs-lookup"><span data-stu-id="94fe3-120">The name of the font.</span></span>  <br/> |
   
## <a name="return-value"></a><span data-ttu-id="94fe3-121">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="94fe3-121">Return value</span></span>

<span data-ttu-id="94fe3-122">Inteiro</span><span class="sxs-lookup"><span data-stu-id="94fe3-122">Integer</span></span>
  
## <a name="remarks"></a><span data-ttu-id="94fe3-123">Comentários</span><span class="sxs-lookup"><span data-stu-id="94fe3-123">Remarks</span></span>

<span data-ttu-id="94fe3-124">Se a cadeia de caracteres fornecida para *font_name_string* não corresponder a uma fonte conhecida, essa função retornará um #VALUE!</span><span class="sxs-lookup"><span data-stu-id="94fe3-124">If the string provided for  *font_name_string*  does not match a known font, this function returns a #VALUE!</span></span> <span data-ttu-id="94fe3-125">erro.</span><span class="sxs-lookup"><span data-stu-id="94fe3-125">error.</span></span> 
  
## <a name="example"></a><span data-ttu-id="94fe3-126">Exemplo</span><span class="sxs-lookup"><span data-stu-id="94fe3-126">Example</span></span>

 `FONT("Calibri")`
  
<span data-ttu-id="94fe3-127">Retorna o valor de inteiro (4) representando a ID exclusiva para a fonte "Calibri".</span><span class="sxs-lookup"><span data-stu-id="94fe3-127">Returns the integer value (4) representing the unique ID for the "Calibri" font.</span></span>
  

