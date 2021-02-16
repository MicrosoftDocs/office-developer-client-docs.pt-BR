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
# <a name="datepart-function-access-custom-web-app"></a><span data-ttu-id="4b3ac-103">Função DatePart (aplicativo Web personalizado do Access)</span><span class="sxs-lookup"><span data-stu-id="4b3ac-103">DatePart function (Access custom web app)</span></span>

<span data-ttu-id="4b3ac-104">Retorna um valor numérico que representa a parte de data especificada da data especificada.</span><span class="sxs-lookup"><span data-stu-id="4b3ac-104">Returns a numeric value that represents the specified date part of the specified date.</span></span>
  
> [!NOTE]
> <span data-ttu-id="4b3ac-105">O recurso de armazenamento em nuvem descrito neste artigo não tem mais suporte no Office 2013 e Office 2016, e pode resultar no seguinte erro: > *Estamos com problemas de servidor, portanto, não podemos adicionar \<serviço\> agora. Tente novamente mais tarde.*</span><span class="sxs-lookup"><span data-stu-id="4b3ac-105">The cloud storage feature described in this article is no longer supported in Office 2013 and Office 2016 and may result in the following error: >  *Sorry, we're having server problems, so we can't add \<service\> right now. Please try again later.*</span></span> <span data-ttu-id="4b3ac-106">> Para armazenamento em nuvem do Office Online, Office para iOS e Office para Android, você poderá pesquisar no nosso [Programa de Parceiros de Armazenamento de Nuvem do Office](https://dev.office.com/programs/officecloudstorage).</span><span class="sxs-lookup"><span data-stu-id="4b3ac-106">> For cloud storage for Office Online, Office for iOS, and Office for Android, you can look into our [Office Cloud Storage Partner Program](https://dev.office.com/programs/officecloudstorage).</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="4b3ac-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="4b3ac-107">Syntax</span></span>

<span data-ttu-id="4b3ac-108">**DatePart** (*DatePart*, *Date*)</span><span class="sxs-lookup"><span data-stu-id="4b3ac-108">**DatePart** (*DatePart*, *Date*)</span></span> 
  
<span data-ttu-id="4b3ac-109">A **função DatePart** contém os seguintes argumentos.</span><span class="sxs-lookup"><span data-stu-id="4b3ac-109">The **DatePart** function contains the following arguments.</span></span> 
  
|<span data-ttu-id="4b3ac-110">**Nome do argumento**</span><span class="sxs-lookup"><span data-stu-id="4b3ac-110">**Argument name**</span></span>|<span data-ttu-id="4b3ac-111">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="4b3ac-111">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="4b3ac-112">*DatePart*</span><span class="sxs-lookup"><span data-stu-id="4b3ac-112">*DatePart*</span></span>  <br/> |<span data-ttu-id="4b3ac-113">A parte de  *Data*  (um valor de data ou hora) para a qual um inteiro será retornado.</span><span class="sxs-lookup"><span data-stu-id="4b3ac-113">The part of  *Date*  (a date or time value) for which an integer will be returned.</span></span> <span data-ttu-id="4b3ac-114">Consulte a seção Comentários para ver a lista de abreviaturas válidas.</span><span class="sxs-lookup"><span data-stu-id="4b3ac-114">Refer to the Remarks section for the list of valid abbreviations.</span></span>  <br/> |
| <span data-ttu-id="4b3ac-115">*Date*</span><span class="sxs-lookup"><span data-stu-id="4b3ac-115">*Date*</span></span>  <br/> |<span data-ttu-id="4b3ac-116">Uma expressão que pode ser resolvida para um valor de Data/Hora.</span><span class="sxs-lookup"><span data-stu-id="4b3ac-116">An expression that can be resolved to a Date/Time value.</span></span> <span data-ttu-id="4b3ac-117">A  *expressão do argumento Date,*  a expressão de coluna, a variável definida pelo usuário ou a cadeia de caracteres literal.</span><span class="sxs-lookup"><span data-stu-id="4b3ac-117">The  *Date*  argument expression, column expression, user-defined variable or string literal.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="4b3ac-118">Comentários</span><span class="sxs-lookup"><span data-stu-id="4b3ac-118">Remarks</span></span>

<span data-ttu-id="4b3ac-119">A tabela a seguir lista todos os  *argumentos DatePart*  válidos.</span><span class="sxs-lookup"><span data-stu-id="4b3ac-119">The following table lists all valid  *DatePart*  arguments.</span></span> 
  
|<span data-ttu-id="4b3ac-120">***DatePart***</span><span class="sxs-lookup"><span data-stu-id="4b3ac-120">***DatePart***</span></span>|
|:-----|
|<span data-ttu-id="4b3ac-121">**ano**</span><span class="sxs-lookup"><span data-stu-id="4b3ac-121">**year**</span></span> <br/> |
|<span data-ttu-id="4b3ac-122">**quarter**</span><span class="sxs-lookup"><span data-stu-id="4b3ac-122">**quarter**</span></span> <br/> |
|<span data-ttu-id="4b3ac-123">**Mês**</span><span class="sxs-lookup"><span data-stu-id="4b3ac-123">**month**</span></span> <br/> |
|<span data-ttu-id="4b3ac-124">**dayofyear**</span><span class="sxs-lookup"><span data-stu-id="4b3ac-124">**dayofyear**</span></span> <br/> |
|<span data-ttu-id="4b3ac-125">**dia**</span><span class="sxs-lookup"><span data-stu-id="4b3ac-125">**day**</span></span> <br/> |
|<span data-ttu-id="4b3ac-126">**semana**</span><span class="sxs-lookup"><span data-stu-id="4b3ac-126">**week**</span></span> <br/> |
|<span data-ttu-id="4b3ac-127">**weekday**</span><span class="sxs-lookup"><span data-stu-id="4b3ac-127">**weekday**</span></span> <br/> |
|<span data-ttu-id="4b3ac-128">**hour**</span><span class="sxs-lookup"><span data-stu-id="4b3ac-128">**hour**</span></span> <br/> |
|<span data-ttu-id="4b3ac-129">**minuto**</span><span class="sxs-lookup"><span data-stu-id="4b3ac-129">**minute**</span></span> <br/> |
|<span data-ttu-id="4b3ac-130">**segundo**</span><span class="sxs-lookup"><span data-stu-id="4b3ac-130">**second**</span></span> <br/> |
|<span data-ttu-id="4b3ac-131">**milissegundos**</span><span class="sxs-lookup"><span data-stu-id="4b3ac-131">**millisecond**</span></span> <br/> |
   

