---
title: Função DateDiff (aplicativo da web personalizado do Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
localization_priority: Normal
ms.assetid: 1c58ee87-0f57-4643-be4d-62da815df705
description: Retorna a contagem dos limites de parte da data especificada ultrapassados entre a data de início especificada e a data de término.
ms.openlocfilehash: fe898ec5eb59cb341250cb0c0e2e35bc55d37eb3
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19765084"
---
# <a name="datediff-function-access-custom-web-app"></a><span data-ttu-id="6da41-103">Função DateDiff (aplicativo da web personalizado do Access)</span><span class="sxs-lookup"><span data-stu-id="6da41-103">DateDiff function (Access custom web app)</span></span>

<span data-ttu-id="6da41-104">Retorna a contagem dos limites de parte da data especificada ultrapassados entre a data de início especificada e a data de término.</span><span class="sxs-lookup"><span data-stu-id="6da41-104">Returns the count of the specified date part boundaries crossed between the specified start date and end date.</span></span>
  
> [!NOTE]
> <span data-ttu-id="6da41-105">O recurso de armazenamento de nuvem descrito neste artigo não é mais suportado no Office 2013 e Office 2016 e pode resultar no seguinte erro: > *Sorry, vamos ter problemas no servidor, portanto não podemos adicionar \<service\> conveniente. Tente novamente mais tarde.*</span><span class="sxs-lookup"><span data-stu-id="6da41-105">The cloud storage feature described in this article is no longer supported in Office 2013 and Office 2016 and may result in the following error: >  *Sorry, we're having server problems, so we can't add \<service\> right now. Please try again later.*</span></span> <span data-ttu-id="6da41-106">> Para armazenamento em nuvem para o Office Online, o Office para iOS e do Office para Android, você pode pesquisar em nosso [Programa de parceria de armazenamento de nuvem do Office](https://dev.office.com/programs/officecloudstorage).</span><span class="sxs-lookup"><span data-stu-id="6da41-106">> For cloud storage for Office Online, Office for iOS, and Office for Android, you can look into our [Office Cloud Storage Partner Program](https://dev.office.com/programs/officecloudstorage).</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="6da41-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="6da41-107">Syntax</span></span>

<span data-ttu-id="6da41-108">**DateDiff** (*DatePart*, *StartDate*, *EndDate*)</span><span class="sxs-lookup"><span data-stu-id="6da41-108">**DateDiff** (*DatePart*, *StartDate*, *EndDate*)</span></span> 
  
<span data-ttu-id="6da41-109">A função **DateDiff** contém os seguintes argumentos.</span><span class="sxs-lookup"><span data-stu-id="6da41-109">The **DateDiff** function contains the following arguments.</span></span> 
  
|<span data-ttu-id="6da41-110">**Nome do argumento**</span><span class="sxs-lookup"><span data-stu-id="6da41-110">**Argument name**</span></span>|<span data-ttu-id="6da41-111">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="6da41-111">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="6da41-112">*DatePart*</span><span class="sxs-lookup"><span data-stu-id="6da41-112">*DatePart*</span></span>  <br/> |<span data-ttu-id="6da41-113">É a parte da *StartDate* e *EndDate* que especifica o tipo de limite ultrapassado.</span><span class="sxs-lookup"><span data-stu-id="6da41-113">Is the part of  *StartDate*  and  *EndDate*  that specifies the type of boundary crossed.</span></span> <span data-ttu-id="6da41-114">Consulte a seção de comentários para a lista das configurações válidas.</span><span class="sxs-lookup"><span data-stu-id="6da41-114">Refer to the Remarks section for the list of valid settings.</span></span>  <br/> |
| <span data-ttu-id="6da41-115">*StartDate*</span><span class="sxs-lookup"><span data-stu-id="6da41-115">*StartDate*</span></span>  <br/> |<span data-ttu-id="6da41-116">Uma expressão que pode ser resolvida como um valor de data/hora.</span><span class="sxs-lookup"><span data-stu-id="6da41-116">An expression that can be resolved to a Date/Time value.</span></span> <span data-ttu-id="6da41-117">A expressão de argumento *Data* , expressão de coluna, a variável definida pelo usuário ou cadeia de caracteres literal.</span><span class="sxs-lookup"><span data-stu-id="6da41-117">The  *Date*  argument expression, column expression, user-defined variable or string literal.</span></span>  <br/> |
| <span data-ttu-id="6da41-118">*EndDate*</span><span class="sxs-lookup"><span data-stu-id="6da41-118">*EndDate*</span></span>  <br/> |<span data-ttu-id="6da41-119">Uma expressão que pode ser resolvida como um valor de data/hora.</span><span class="sxs-lookup"><span data-stu-id="6da41-119">An expression that can be resolved to a Date/Time value.</span></span> <span data-ttu-id="6da41-120">A expressão de argumento *Data* , expressão de coluna, a variável definida pelo usuário ou cadeia de caracteres literal.</span><span class="sxs-lookup"><span data-stu-id="6da41-120">The  *Date*  argument expression, column expression, user-defined variable or string literal.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="6da41-121">Coment�rios</span><span class="sxs-lookup"><span data-stu-id="6da41-121">Remarks</span></span>

<span data-ttu-id="6da41-122">A tabela a seguir lista todos os argumentos *DatePart* válidos.</span><span class="sxs-lookup"><span data-stu-id="6da41-122">The following table lists all valid  *DatePart*  arguments.</span></span> 
  
|<span data-ttu-id="6da41-123">***DatePart***</span><span class="sxs-lookup"><span data-stu-id="6da41-123">***DatePart***</span></span>|
|:-----|
|<span data-ttu-id="6da41-124">**year**</span><span class="sxs-lookup"><span data-stu-id="6da41-124">**year**</span></span> <br/> |
|<span data-ttu-id="6da41-125">**trimestre**</span><span class="sxs-lookup"><span data-stu-id="6da41-125">**quarter**</span></span> <br/> |
|<span data-ttu-id="6da41-126">**Mês**</span><span class="sxs-lookup"><span data-stu-id="6da41-126">**month**</span></span> <br/> |
|<span data-ttu-id="6da41-127">**DAYOFYEAR**</span><span class="sxs-lookup"><span data-stu-id="6da41-127">**dayofyear**</span></span> <br/> |
|<span data-ttu-id="6da41-128">**day**</span><span class="sxs-lookup"><span data-stu-id="6da41-128">**day**</span></span> <br/> |
|<span data-ttu-id="6da41-129">**semana**</span><span class="sxs-lookup"><span data-stu-id="6da41-129">**week**</span></span> <br/> |
|<span data-ttu-id="6da41-130">**hora**</span><span class="sxs-lookup"><span data-stu-id="6da41-130">**hour**</span></span> <br/> |
|<span data-ttu-id="6da41-131">**minuto**</span><span class="sxs-lookup"><span data-stu-id="6da41-131">**minute**</span></span> <br/> |
|<span data-ttu-id="6da41-132">**segundo**</span><span class="sxs-lookup"><span data-stu-id="6da41-132">**second**</span></span> <br/> |
|<span data-ttu-id="6da41-133">**milissegundo**</span><span class="sxs-lookup"><span data-stu-id="6da41-133">**millisecond**</span></span> <br/> |
   

