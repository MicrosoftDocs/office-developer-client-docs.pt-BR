---
title: Função DateDiff (aplicativo Web personalizado do Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
localization_priority: Normal
ms.assetid: 1c58ee87-0f57-4643-be4d-62da815df705
description: Retorna a contagem dos limites de parte de data especificados cruzados entre a data de início e a data de término especificadas.
ms.openlocfilehash: 1cce8a501c5a57384372e681f903baa4f4c20bef
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32280718"
---
# <a name="datediff-function-access-custom-web-app"></a><span data-ttu-id="49730-103">Função DateDiff (aplicativo Web personalizado do Access)</span><span class="sxs-lookup"><span data-stu-id="49730-103">DateDiff function (Access custom web app)</span></span>

<span data-ttu-id="49730-104">Retorna a contagem dos limites de parte de data especificados cruzados entre a data de início e a data de término especificadas.</span><span class="sxs-lookup"><span data-stu-id="49730-104">Returns the count of the specified date part boundaries crossed between the specified start date and end date.</span></span>
  
> [!NOTE]
> <span data-ttu-id="49730-105">O recurso de armazenamento em nuvem descrito neste artigo não tem mais suporte no Office 2013 e Office 2016, e pode resultar no seguinte erro: > *Estamos com problemas de servidor, portanto, não podemos adicionar \<serviço\> agora. Tente novamente mais tarde.*</span><span class="sxs-lookup"><span data-stu-id="49730-105">The cloud storage feature described in this article is no longer supported in Office 2013 and Office 2016 and may result in the following error: >  *Sorry, we're having server problems, so we can't add \<service\> right now. Please try again later.*</span></span> <span data-ttu-id="49730-106">> Para armazenamento em nuvem do Office Online, Office para iOS e Office para Android, você poderá pesquisar no nosso [Programa de Parceiros de Armazenamento de Nuvem do Office](https://dev.office.com/programs/officecloudstorage).</span><span class="sxs-lookup"><span data-stu-id="49730-106">> For cloud storage for Office Online, Office for iOS, and Office for Android, you can look into our [Office Cloud Storage Partner Program](https://dev.office.com/programs/officecloudstorage).</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="49730-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="49730-107">Syntax</span></span>

<span data-ttu-id="49730-108">**DateDiff** (*Datepart*, *StartDate*, *EndDate*)</span><span class="sxs-lookup"><span data-stu-id="49730-108">**DateDiff** (*DatePart*, *StartDate*, *EndDate*)</span></span> 
  
<span data-ttu-id="49730-109">A função **DateDiff** contém os seguintes argumentos.</span><span class="sxs-lookup"><span data-stu-id="49730-109">The **DateDiff** function contains the following arguments.</span></span> 
  
|<span data-ttu-id="49730-110">**Nome do argumento**</span><span class="sxs-lookup"><span data-stu-id="49730-110">**Argument name**</span></span>|<span data-ttu-id="49730-111">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="49730-111">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="49730-112">*DatePart*</span><span class="sxs-lookup"><span data-stu-id="49730-112">*DatePart*</span></span>  <br/> |<span data-ttu-id="49730-113">É a parte de *StartDate* e *EndDate* que especifica o tipo de limite ultrapassado.</span><span class="sxs-lookup"><span data-stu-id="49730-113">Is the part of  *StartDate*  and  *EndDate*  that specifies the type of boundary crossed.</span></span> <span data-ttu-id="49730-114">Consulte a seção comentários para obter a lista de configurações válidas.</span><span class="sxs-lookup"><span data-stu-id="49730-114">Refer to the Remarks section for the list of valid settings.</span></span>  <br/> |
| <span data-ttu-id="49730-115">*StartDate*</span><span class="sxs-lookup"><span data-stu-id="49730-115">*StartDate*</span></span>  <br/> |<span data-ttu-id="49730-116">Uma expressão que pode ser resolvida como um valor de data/hora.</span><span class="sxs-lookup"><span data-stu-id="49730-116">An expression that can be resolved to a Date/Time value.</span></span> <span data-ttu-id="49730-117">A expressão de argumento de *Data* , expressão de coluna, variável definida pelo usuário ou literal de cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="49730-117">The  *Date*  argument expression, column expression, user-defined variable or string literal.</span></span>  <br/> |
| <span data-ttu-id="49730-118">*EndDate*</span><span class="sxs-lookup"><span data-stu-id="49730-118">*EndDate*</span></span>  <br/> |<span data-ttu-id="49730-119">Uma expressão que pode ser resolvida como um valor de data/hora.</span><span class="sxs-lookup"><span data-stu-id="49730-119">An expression that can be resolved to a Date/Time value.</span></span> <span data-ttu-id="49730-120">A expressão de argumento de *Data* , expressão de coluna, variável definida pelo usuário ou literal de cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="49730-120">The  *Date*  argument expression, column expression, user-defined variable or string literal.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="49730-121">Comentários</span><span class="sxs-lookup"><span data-stu-id="49730-121">Remarks</span></span>

<span data-ttu-id="49730-122">A tabela a seguir lista todos os argumentos de *datepart* válidos.</span><span class="sxs-lookup"><span data-stu-id="49730-122">The following table lists all valid  *DatePart*  arguments.</span></span> 
  
|<span data-ttu-id="49730-123">***DatePart***</span><span class="sxs-lookup"><span data-stu-id="49730-123">***DatePart***</span></span>|
|:-----|
|<span data-ttu-id="49730-124">**year**</span><span class="sxs-lookup"><span data-stu-id="49730-124">**year**</span></span> <br/> |
|<span data-ttu-id="49730-125">**trimestre**</span><span class="sxs-lookup"><span data-stu-id="49730-125">**quarter**</span></span> <br/> |
|<span data-ttu-id="49730-126">**Mês**</span><span class="sxs-lookup"><span data-stu-id="49730-126">**month**</span></span> <br/> |
|<span data-ttu-id="49730-127">**DayOfYear**</span><span class="sxs-lookup"><span data-stu-id="49730-127">**dayofyear**</span></span> <br/> |
|<span data-ttu-id="49730-128">**day**</span><span class="sxs-lookup"><span data-stu-id="49730-128">**day**</span></span> <br/> |
|<span data-ttu-id="49730-129">**útil**</span><span class="sxs-lookup"><span data-stu-id="49730-129">**week**</span></span> <br/> |
|<span data-ttu-id="49730-130">**hora**</span><span class="sxs-lookup"><span data-stu-id="49730-130">**hour**</span></span> <br/> |
|<span data-ttu-id="49730-131">**inclusões**</span><span class="sxs-lookup"><span data-stu-id="49730-131">**minute**</span></span> <br/> |
|<span data-ttu-id="49730-132">**secundária**</span><span class="sxs-lookup"><span data-stu-id="49730-132">**second**</span></span> <br/> |
|<span data-ttu-id="49730-133">**milissegundo**</span><span class="sxs-lookup"><span data-stu-id="49730-133">**millisecond**</span></span> <br/> |
   

