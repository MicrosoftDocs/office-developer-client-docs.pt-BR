---
title: Função DateWithTimeFromParts (aplicativo Web personalizado do Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
localization_priority: Normal
ms.assetid: aa97cbaa-8b14-42e3-a098-938ebe0769eb
description: Retorna uma Data e Hora com base em um ano, mês, dia e hora especificados.
ms.openlocfilehash: ee995d346ca27e683f342cf3f611c1147997d24e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422086"
---
# <a name="datewithtimefromparts-function-access-custom-web-app"></a><span data-ttu-id="181b6-103">Função DateWithTimeFromParts (aplicativo Web personalizado do Access)</span><span class="sxs-lookup"><span data-stu-id="181b6-103">DateWithTimeFromParts function (Access custom web app)</span></span>

<span data-ttu-id="181b6-104">Retorna uma Data e Hora com base em um ano, mês, dia e hora especificados.</span><span class="sxs-lookup"><span data-stu-id="181b6-104">Returns a Date and Time based on a specified year, month, day, and time.</span></span>
  
> [!NOTE]
> <span data-ttu-id="181b6-105">O recurso de armazenamento em nuvem descrito neste artigo não tem mais suporte no Office 2013 e Office 2016, e pode resultar no seguinte erro: > *Estamos com problemas de servidor, portanto, não podemos adicionar \<serviço\> agora. Tente novamente mais tarde.*</span><span class="sxs-lookup"><span data-stu-id="181b6-105">The cloud storage feature described in this article is no longer supported in Office 2013 and Office 2016 and may result in the following error: >  *Sorry, we're having server problems, so we can't add \<service\> right now. Please try again later.*</span></span> <span data-ttu-id="181b6-106">> Para armazenamento em nuvem do Office Online, Office para iOS e Office para Android, você poderá pesquisar no nosso [Programa de Parceiros de Armazenamento de Nuvem do Office](https://dev.office.com/programs/officecloudstorage).</span><span class="sxs-lookup"><span data-stu-id="181b6-106">> For cloud storage for Office Online, Office for iOS, and Office for Android, you can look into our [Office Cloud Storage Partner Program](https://dev.office.com/programs/officecloudstorage).</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="181b6-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="181b6-107">Syntax</span></span>

<span data-ttu-id="181b6-108">**DateWithTimeFromParts** (*Ano*, *Mês*, *Dia*, *Hora*, *Minuto*, *Segundo*)</span><span class="sxs-lookup"><span data-stu-id="181b6-108">**DateWithTimeFromParts** (*Year*, *Month*, *Day*, *Hour*, *Minute*, *Second*)</span></span> 
  
<span data-ttu-id="181b6-109">A **função DateWithTimeFromParts** contém os seguintes argumentos.</span><span class="sxs-lookup"><span data-stu-id="181b6-109">The **DateWithTimeFromParts** function contains the following arguments.</span></span> 
  
|<span data-ttu-id="181b6-110">**Nome do argumento**</span><span class="sxs-lookup"><span data-stu-id="181b6-110">**Argument name**</span></span>|<span data-ttu-id="181b6-111">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="181b6-111">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="181b6-112">*Year*</span><span class="sxs-lookup"><span data-stu-id="181b6-112">*Year*</span></span>  <br/> |<span data-ttu-id="181b6-113">Expressão inteira especificando um ano.</span><span class="sxs-lookup"><span data-stu-id="181b6-113">Integer expression specifying a year.</span></span>  <br/> |
| <span data-ttu-id="181b6-114">*Month*</span><span class="sxs-lookup"><span data-stu-id="181b6-114">*Month*</span></span>  <br/> |<span data-ttu-id="181b6-115">Expressão inteira especificando um mês.</span><span class="sxs-lookup"><span data-stu-id="181b6-115">Integer expression specifying a month.</span></span>  <br/> |
| <span data-ttu-id="181b6-116">*Day*</span><span class="sxs-lookup"><span data-stu-id="181b6-116">*Day*</span></span>  <br/> |<span data-ttu-id="181b6-117">Expressão inteira especificando um dia.</span><span class="sxs-lookup"><span data-stu-id="181b6-117">Integer expression specifying a day.</span></span>  <br/> |
| <span data-ttu-id="181b6-118">*Hour*</span><span class="sxs-lookup"><span data-stu-id="181b6-118">*Hour*</span></span>  <br/> |<span data-ttu-id="181b6-119">Expressão inteira especificando horas.</span><span class="sxs-lookup"><span data-stu-id="181b6-119">Integer expression specifying hours.</span></span>  <br/> |
| <span data-ttu-id="181b6-120">*Minute*</span><span class="sxs-lookup"><span data-stu-id="181b6-120">*Minute*</span></span>  <br/> |<span data-ttu-id="181b6-121">Expressão inteira especificando minutos.</span><span class="sxs-lookup"><span data-stu-id="181b6-121">Integer expression specifying minutes.</span></span>  <br/> |
| <span data-ttu-id="181b6-122">*Second*</span><span class="sxs-lookup"><span data-stu-id="181b6-122">*Second*</span></span>  <br/> |<span data-ttu-id="181b6-123">Expressão inteira especificando segundos.</span><span class="sxs-lookup"><span data-stu-id="181b6-123">Integer expression specifying seconds.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="181b6-124">Comentários</span><span class="sxs-lookup"><span data-stu-id="181b6-124">Remarks</span></span>

<span data-ttu-id="181b6-125">**DateWithTimeFromParts** retorna um valor de Data/Hora totalmente inicializado.</span><span class="sxs-lookup"><span data-stu-id="181b6-125">**DateWithTimeFromParts** returns a fully initialized Date/Time value.</span></span> <span data-ttu-id="181b6-126">Se os argumentos não são válidos, um erro é gerado.</span><span class="sxs-lookup"><span data-stu-id="181b6-126">If the arguments are not valid, an error is raised.</span></span> <span data-ttu-id="181b6-127">Se os argumentos necessários são Nulos, Null é retornado.</span><span class="sxs-lookup"><span data-stu-id="181b6-127">If required arguments are Null, then Null is returned.</span></span> 
  

