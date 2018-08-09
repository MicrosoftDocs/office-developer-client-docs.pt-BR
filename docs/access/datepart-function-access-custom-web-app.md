---
title: Função DatePart (aplicativo da web personalizado do Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
localization_priority: Normal
ms.assetid: 8936f0b6-f9b2-44ef-bf90-e482b64611cd
description: Retorna um valor numérico que representa a parte da data especificada da data especificada.
ms.openlocfilehash: 81aa1880e5b38c33f75018418a44ed82e5e7e8c0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19765042"
---
# <a name="datepart-function-access-custom-web-app"></a><span data-ttu-id="720eb-103">Função DatePart (aplicativo da web personalizado do Access)</span><span class="sxs-lookup"><span data-stu-id="720eb-103">DatePart function (Access custom web app)</span></span>

<span data-ttu-id="720eb-104">Retorna um valor numérico que representa a parte da data especificada da data especificada.</span><span class="sxs-lookup"><span data-stu-id="720eb-104">Returns a numeric value that represents the specified date part of the specified date.</span></span>
  
> [!NOTE]
> <span data-ttu-id="720eb-105">O recurso de armazenamento de nuvem descrito neste artigo não é mais suportado no Office 2013 e Office 2016 e pode resultar no seguinte erro: > *Sorry, vamos ter problemas no servidor, portanto não podemos adicionar \<service\> conveniente. Tente novamente mais tarde.*</span><span class="sxs-lookup"><span data-stu-id="720eb-105">The cloud storage feature described in this article is no longer supported in Office 2013 and Office 2016 and may result in the following error: >  *Sorry, we're having server problems, so we can't add \<service\> right now. Please try again later.*</span></span> <span data-ttu-id="720eb-106">> Para armazenamento em nuvem para o Office Online, o Office para iOS e do Office para Android, você pode pesquisar em nosso [Programa de parceria de armazenamento de nuvem do Office](https://dev.office.com/programs/officecloudstorage).</span><span class="sxs-lookup"><span data-stu-id="720eb-106">> For cloud storage for Office Online, Office for iOS, and Office for Android, you can look into our [Office Cloud Storage Partner Program](https://dev.office.com/programs/officecloudstorage).</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="720eb-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="720eb-107">Syntax</span></span>

<span data-ttu-id="720eb-108">**DatePart** (*DatePart*, *Data*)</span><span class="sxs-lookup"><span data-stu-id="720eb-108">**DatePart** (*DatePart*, *Date*)</span></span> 
  
<span data-ttu-id="720eb-109">A função **PartData** contém os seguintes argumentos.</span><span class="sxs-lookup"><span data-stu-id="720eb-109">The **DatePart** function contains the following arguments.</span></span> 
  
|<span data-ttu-id="720eb-110">**Nome do argumento**</span><span class="sxs-lookup"><span data-stu-id="720eb-110">**Argument name**</span></span>|<span data-ttu-id="720eb-111">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="720eb-111">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="720eb-112">*ParteDeData*</span><span class="sxs-lookup"><span data-stu-id="720eb-112">*DatePart*</span></span>  <br/> |<span data-ttu-id="720eb-113">A parte de *Data* (um valor de data ou hora) para o qual será retornado um número inteiro.</span><span class="sxs-lookup"><span data-stu-id="720eb-113">The part of  *Date*  (a date or time value) for which an integer will be returned.</span></span> <span data-ttu-id="720eb-114">Consulte a seção de comentários para a lista de abreviações válidas.</span><span class="sxs-lookup"><span data-stu-id="720eb-114">Refer to the Remarks section for the list of valid abbreviations.</span></span>  <br/> |
| <span data-ttu-id="720eb-115">*Date*</span><span class="sxs-lookup"><span data-stu-id="720eb-115">*Date*</span></span>  <br/> |<span data-ttu-id="720eb-116">Uma expressão que pode ser resolvida como um valor de data/hora.</span><span class="sxs-lookup"><span data-stu-id="720eb-116">An expression that can be resolved to a Date/Time value.</span></span> <span data-ttu-id="720eb-117">A expressão de argumento *Data* , expressão de coluna, a variável definida pelo usuário ou cadeia de caracteres literal.</span><span class="sxs-lookup"><span data-stu-id="720eb-117">The  *Date*  argument expression, column expression, user-defined variable or string literal.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="720eb-118">Comentários</span><span class="sxs-lookup"><span data-stu-id="720eb-118">Remarks</span></span>

<span data-ttu-id="720eb-119">A tabela a seguir lista todos os argumentos *DatePart* válidos.</span><span class="sxs-lookup"><span data-stu-id="720eb-119">The following table lists all valid  *DatePart*  arguments.</span></span> 
  
|<span data-ttu-id="720eb-120">***ParteDeData***</span><span class="sxs-lookup"><span data-stu-id="720eb-120">***DatePart***</span></span>|
|:-----|
|<span data-ttu-id="720eb-121">**year**</span><span class="sxs-lookup"><span data-stu-id="720eb-121">**year**</span></span> <br/> |
|<span data-ttu-id="720eb-122">**trimestre**</span><span class="sxs-lookup"><span data-stu-id="720eb-122">**quarter**</span></span> <br/> |
|<span data-ttu-id="720eb-123">**Mês**</span><span class="sxs-lookup"><span data-stu-id="720eb-123">**month**</span></span> <br/> |
|<span data-ttu-id="720eb-124">**DAYOFYEAR**</span><span class="sxs-lookup"><span data-stu-id="720eb-124">**dayofyear**</span></span> <br/> |
|<span data-ttu-id="720eb-125">**day**</span><span class="sxs-lookup"><span data-stu-id="720eb-125">**day**</span></span> <br/> |
|<span data-ttu-id="720eb-126">**semana**</span><span class="sxs-lookup"><span data-stu-id="720eb-126">**week**</span></span> <br/> |
|<span data-ttu-id="720eb-127">**Weekday**</span><span class="sxs-lookup"><span data-stu-id="720eb-127">**weekday**</span></span> <br/> |
|<span data-ttu-id="720eb-128">**hora**</span><span class="sxs-lookup"><span data-stu-id="720eb-128">**hour**</span></span> <br/> |
|<span data-ttu-id="720eb-129">**minuto**</span><span class="sxs-lookup"><span data-stu-id="720eb-129">**minute**</span></span> <br/> |
|<span data-ttu-id="720eb-130">**segundo**</span><span class="sxs-lookup"><span data-stu-id="720eb-130">**second**</span></span> <br/> |
|<span data-ttu-id="720eb-131">**milissegundo**</span><span class="sxs-lookup"><span data-stu-id="720eb-131">**millisecond**</span></span> <br/> |
   

