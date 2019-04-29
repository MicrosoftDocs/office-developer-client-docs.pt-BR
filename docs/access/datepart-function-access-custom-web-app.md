---
title: Função DatePart (aplicativo Web personalizado do Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
localization_priority: Normal
ms.assetid: 8936f0b6-f9b2-44ef-bf90-e482b64611cd
description: Retorna um valor numérico que representa a parte de data especificada da data especificada.
ms.openlocfilehash: 31ac6423614afd61ed943bb7ba375f14696df1ea
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33411432"
---
# <a name="datepart-function-access-custom-web-app"></a><span data-ttu-id="a6e97-103">Função DatePart (aplicativo Web personalizado do Access)</span><span class="sxs-lookup"><span data-stu-id="a6e97-103">DatePart function (Access custom web app)</span></span>

<span data-ttu-id="a6e97-104">Retorna um valor numérico que representa a parte de data especificada da data especificada.</span><span class="sxs-lookup"><span data-stu-id="a6e97-104">Returns a numeric value that represents the specified date part of the specified date.</span></span>
  
> [!NOTE]
> <span data-ttu-id="a6e97-105">O recurso de armazenamento em nuvem descrito neste artigo não tem mais suporte no Office 2013 e Office 2016, e pode resultar no seguinte erro: > *Estamos com problemas de servidor, portanto, não podemos adicionar \<serviço\> agora. Tente novamente mais tarde.*</span><span class="sxs-lookup"><span data-stu-id="a6e97-105">The cloud storage feature described in this article is no longer supported in Office 2013 and Office 2016 and may result in the following error: >  *Sorry, we're having server problems, so we can't add \<service\> right now. Please try again later.*</span></span> <span data-ttu-id="a6e97-106">> Para armazenamento em nuvem do Office Online, Office para iOS e Office para Android, você poderá pesquisar no nosso [Programa de Parceiros de Armazenamento de Nuvem do Office](https://dev.office.com/programs/officecloudstorage).</span><span class="sxs-lookup"><span data-stu-id="a6e97-106">> For cloud storage for Office Online, Office for iOS, and Office for Android, you can look into our [Office Cloud Storage Partner Program](https://dev.office.com/programs/officecloudstorage).</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="a6e97-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a6e97-107">Syntax</span></span>

<span data-ttu-id="a6e97-108">**Datepart** (*Datepart*, *Data*)</span><span class="sxs-lookup"><span data-stu-id="a6e97-108">**DatePart** (*DatePart*, *Date*)</span></span> 
  
<span data-ttu-id="a6e97-109">A função **PartData** contém os seguintes argumentos.</span><span class="sxs-lookup"><span data-stu-id="a6e97-109">The **DatePart** function contains the following arguments.</span></span> 
  
|<span data-ttu-id="a6e97-110">**Nome do argumento**</span><span class="sxs-lookup"><span data-stu-id="a6e97-110">**Argument name**</span></span>|<span data-ttu-id="a6e97-111">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="a6e97-111">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="a6e97-112">*DatePart*</span><span class="sxs-lookup"><span data-stu-id="a6e97-112">*DatePart*</span></span>  <br/> |<span data-ttu-id="a6e97-113">A parte da *Data* (um valor de data ou hora) para a qual um inteiro será retornado.</span><span class="sxs-lookup"><span data-stu-id="a6e97-113">The part of  *Date*  (a date or time value) for which an integer will be returned.</span></span> <span data-ttu-id="a6e97-114">Consulte a seção comentários para obter a lista de abreviações válidas.</span><span class="sxs-lookup"><span data-stu-id="a6e97-114">Refer to the Remarks section for the list of valid abbreviations.</span></span>  <br/> |
| <span data-ttu-id="a6e97-115">*Date*</span><span class="sxs-lookup"><span data-stu-id="a6e97-115">*Date*</span></span>  <br/> |<span data-ttu-id="a6e97-116">Uma expressão que pode ser resolvida como um valor de data/hora.</span><span class="sxs-lookup"><span data-stu-id="a6e97-116">An expression that can be resolved to a Date/Time value.</span></span> <span data-ttu-id="a6e97-117">A expressão de argumento de *Data* , expressão de coluna, variável definida pelo usuário ou literal de cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="a6e97-117">The  *Date*  argument expression, column expression, user-defined variable or string literal.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a6e97-118">Comentários</span><span class="sxs-lookup"><span data-stu-id="a6e97-118">Remarks</span></span>

<span data-ttu-id="a6e97-119">A tabela a seguir lista todos os argumentos de *datepart* válidos.</span><span class="sxs-lookup"><span data-stu-id="a6e97-119">The following table lists all valid  *DatePart*  arguments.</span></span> 
  
|<span data-ttu-id="a6e97-120">***DatePart***</span><span class="sxs-lookup"><span data-stu-id="a6e97-120">***DatePart***</span></span>|
|:-----|
|<span data-ttu-id="a6e97-121">**year**</span><span class="sxs-lookup"><span data-stu-id="a6e97-121">**year**</span></span> <br/> |
|<span data-ttu-id="a6e97-122">**trimestre**</span><span class="sxs-lookup"><span data-stu-id="a6e97-122">**quarter**</span></span> <br/> |
|<span data-ttu-id="a6e97-123">**Mês**</span><span class="sxs-lookup"><span data-stu-id="a6e97-123">**month**</span></span> <br/> |
|<span data-ttu-id="a6e97-124">**DayOfYear**</span><span class="sxs-lookup"><span data-stu-id="a6e97-124">**dayofyear**</span></span> <br/> |
|<span data-ttu-id="a6e97-125">**day**</span><span class="sxs-lookup"><span data-stu-id="a6e97-125">**day**</span></span> <br/> |
|<span data-ttu-id="a6e97-126">**útil**</span><span class="sxs-lookup"><span data-stu-id="a6e97-126">**week**</span></span> <br/> |
|<span data-ttu-id="a6e97-127">**Weekday**</span><span class="sxs-lookup"><span data-stu-id="a6e97-127">**weekday**</span></span> <br/> |
|<span data-ttu-id="a6e97-128">**hora**</span><span class="sxs-lookup"><span data-stu-id="a6e97-128">**hour**</span></span> <br/> |
|<span data-ttu-id="a6e97-129">**inclusões**</span><span class="sxs-lookup"><span data-stu-id="a6e97-129">**minute**</span></span> <br/> |
|<span data-ttu-id="a6e97-130">**secundária**</span><span class="sxs-lookup"><span data-stu-id="a6e97-130">**second**</span></span> <br/> |
|<span data-ttu-id="a6e97-131">**milissegundo**</span><span class="sxs-lookup"><span data-stu-id="a6e97-131">**millisecond**</span></span> <br/> |
   

