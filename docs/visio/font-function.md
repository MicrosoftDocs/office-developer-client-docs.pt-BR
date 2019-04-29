---
title: Função FONT
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 20b587ee-87bf-4648-99ec-ddedd703d9fd
description: Retorna o valor inteiro do identificador exclusivo para uma fonte, especificado por Name.
ms.openlocfilehash: 7ae6fe6dc8bb9c718a358d11d4a6a0227eaf18df
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422170"
---
# <a name="font-function"></a><span data-ttu-id="ab3cd-103">Função FONT</span><span class="sxs-lookup"><span data-stu-id="ab3cd-103">FONT Function</span></span>

<span data-ttu-id="ab3cd-104">Retorna o valor inteiro do identificador exclusivo para uma fonte, especificado por Name.</span><span class="sxs-lookup"><span data-stu-id="ab3cd-104">Returns the integer value of the unique identifier for a font, specified by name.</span></span>
  
> [!NOTE]
> <span data-ttu-id="ab3cd-105">Na maioria dos casos, o identificador de fonte é específico do sistema.</span><span class="sxs-lookup"><span data-stu-id="ab3cd-105">In most cases, the font identifier is system-specific.</span></span> <span data-ttu-id="ab3cd-106">Embora a fonte permaneça estabelecida após ser usada em um arquivo, a função **Font** fornece acesso consistente a uma fonte específica em sistemas e versões do Visio.</span><span class="sxs-lookup"><span data-stu-id="ab3cd-106">Although the font remains established once used in a file, the **FONT** function provides consistent access to a particular font across systems and versions of Visio.</span></span> <span data-ttu-id="ab3cd-107">É recomendável que você use a função **Font** para atribuir fontes em vez de referir-se a identificadores de fonte diretamente.</span><span class="sxs-lookup"><span data-stu-id="ab3cd-107">It is recommended that you use the **FONT** function to assign fonts instead of referring to font identifiers directly.</span></span> 
  
## <a name="version-information"></a><span data-ttu-id="ab3cd-108">Informações sobre a versão</span><span class="sxs-lookup"><span data-stu-id="ab3cd-108">Version Information</span></span>

<span data-ttu-id="ab3cd-109">Version Added: Visio 2013
</span><span class="sxs-lookup"><span data-stu-id="ab3cd-109">Version Added: Visio 2013</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="ab3cd-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ab3cd-110">Syntax</span></span>

 <span data-ttu-id="ab3cd-111">**Fonte** ( _"font_name_string"_)</span><span class="sxs-lookup"><span data-stu-id="ab3cd-111">**FONT**( _"font_name_string"_)</span></span>
  
### <a name="parameters"></a><span data-ttu-id="ab3cd-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ab3cd-112">Parameters</span></span>

|<span data-ttu-id="ab3cd-113">**Name**</span><span class="sxs-lookup"><span data-stu-id="ab3cd-113">**Name**</span></span>|<span data-ttu-id="ab3cd-114">**Obrigatório/opcional**</span><span class="sxs-lookup"><span data-stu-id="ab3cd-114">**Required/Optional**</span></span>|<span data-ttu-id="ab3cd-115">**Tipo de dados**</span><span class="sxs-lookup"><span data-stu-id="ab3cd-115">**Data Type**</span></span>|<span data-ttu-id="ab3cd-116">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="ab3cd-116">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="ab3cd-117">_font_name_string_</span><span class="sxs-lookup"><span data-stu-id="ab3cd-117">_font_name_string_</span></span> <br/> |<span data-ttu-id="ab3cd-118">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="ab3cd-118">Required</span></span>  <br/> |<span data-ttu-id="ab3cd-119">**cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="ab3cd-119">**string**</span></span> <br/> |<span data-ttu-id="ab3cd-120">O nome da fonte.</span><span class="sxs-lookup"><span data-stu-id="ab3cd-120">The name of the font.</span></span>  <br/> |
   
## <a name="return-value"></a><span data-ttu-id="ab3cd-121">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="ab3cd-121">Return value</span></span>

<span data-ttu-id="ab3cd-122">Inteiro</span><span class="sxs-lookup"><span data-stu-id="ab3cd-122">Integer</span></span>
  
## <a name="remarks"></a><span data-ttu-id="ab3cd-123">Comentários</span><span class="sxs-lookup"><span data-stu-id="ab3cd-123">Remarks</span></span>

<span data-ttu-id="ab3cd-124">Se a cadeia de caracteres fornecida para *font_name_string* não corresponder a uma fonte conhecida, esta função retornará um #VALUE!</span><span class="sxs-lookup"><span data-stu-id="ab3cd-124">If the string provided for  *font_name_string*  does not match a known font, this function returns a #VALUE!</span></span> <span data-ttu-id="ab3cd-125">#NUM!</span><span class="sxs-lookup"><span data-stu-id="ab3cd-125">error.</span></span> 
  
## <a name="example"></a><span data-ttu-id="ab3cd-126">Exemplo</span><span class="sxs-lookup"><span data-stu-id="ab3cd-126">Example</span></span>

 `FONT("Calibri")`
  
<span data-ttu-id="ab3cd-127">Retorna o valor inteiro (4) que representa a identificação exclusiva da fonte "Calibri".</span><span class="sxs-lookup"><span data-stu-id="ab3cd-127">Returns the integer value (4) representing the unique ID for the "Calibri" font.</span></span>
  

