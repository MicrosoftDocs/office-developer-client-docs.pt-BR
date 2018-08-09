---
title: Função DateWithTimeFromParts (aplicativo da web personalizado do Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
localization_priority: Normal
ms.assetid: aa97cbaa-8b14-42e3-a098-938ebe0769eb
description: Retorna uma data e hora com base em um ano especificado, mês, dia e hora.
ms.openlocfilehash: 8cc1fbe700d18c04d944793bcea889424b0cff3f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19765030"
---
# <a name="datewithtimefromparts-function-access-custom-web-app"></a><span data-ttu-id="6a501-103">Função DateWithTimeFromParts (aplicativo da web personalizado do Access)</span><span class="sxs-lookup"><span data-stu-id="6a501-103">DateWithTimeFromParts function (Access custom web app)</span></span>

<span data-ttu-id="6a501-104">Retorna uma data e hora com base em um ano especificado, mês, dia e hora.</span><span class="sxs-lookup"><span data-stu-id="6a501-104">Returns a Date and Time based on a specified year, month, day, and time.</span></span>
  
> [!NOTE]
> <span data-ttu-id="6a501-105">O recurso de armazenamento de nuvem descrito neste artigo não é mais suportado no Office 2013 e Office 2016 e pode resultar no seguinte erro: > *Sorry, vamos ter problemas no servidor, portanto não podemos adicionar \<service\> conveniente. Tente novamente mais tarde.*</span><span class="sxs-lookup"><span data-stu-id="6a501-105">The cloud storage feature described in this article is no longer supported in Office 2013 and Office 2016 and may result in the following error: >  *Sorry, we're having server problems, so we can't add \<service\> right now. Please try again later.*</span></span> <span data-ttu-id="6a501-106">> Para armazenamento em nuvem para o Office Online, o Office para iOS e do Office para Android, você pode pesquisar em nosso [Programa de parceria de armazenamento de nuvem do Office](https://dev.office.com/programs/officecloudstorage).</span><span class="sxs-lookup"><span data-stu-id="6a501-106">> For cloud storage for Office Online, Office for iOS, and Office for Android, you can look into our [Office Cloud Storage Partner Program](https://dev.office.com/programs/officecloudstorage).</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="6a501-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="6a501-107">Syntax</span></span>

<span data-ttu-id="6a501-108">**DateWithTimeFromParts** (*Ano*, *mês*, *dia*, *hora*, *minuto*, *segundo*)</span><span class="sxs-lookup"><span data-stu-id="6a501-108">**DateWithTimeFromParts** (*Year*, *Month*, *Day*, *Hour*, *Minute*, *Second*)</span></span> 
  
<span data-ttu-id="6a501-109">A função **DateWithTimeFromParts** contém os seguintes argumentos.</span><span class="sxs-lookup"><span data-stu-id="6a501-109">The **DateWithTimeFromParts** function contains the following arguments.</span></span> 
  
|<span data-ttu-id="6a501-110">**Nome do argumento**</span><span class="sxs-lookup"><span data-stu-id="6a501-110">**Argument name**</span></span>|<span data-ttu-id="6a501-111">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="6a501-111">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="6a501-112">*Ano*</span><span class="sxs-lookup"><span data-stu-id="6a501-112">*Year*</span></span>  <br/> |<span data-ttu-id="6a501-113">Expressão de inteiro especificando um ano.</span><span class="sxs-lookup"><span data-stu-id="6a501-113">Integer expression specifying a year.</span></span>  <br/> |
| <span data-ttu-id="6a501-114">*Month*</span><span class="sxs-lookup"><span data-stu-id="6a501-114">*Month*</span></span>  <br/> |<span data-ttu-id="6a501-115">Expressão de inteiro especificando um mês.</span><span class="sxs-lookup"><span data-stu-id="6a501-115">Integer expression specifying a month.</span></span>  <br/> |
| <span data-ttu-id="6a501-116">*Dia*</span><span class="sxs-lookup"><span data-stu-id="6a501-116">*Day*</span></span>  <br/> |<span data-ttu-id="6a501-117">Expressão de inteiro especificando um dia.</span><span class="sxs-lookup"><span data-stu-id="6a501-117">Integer expression specifying a day.</span></span>  <br/> |
| <span data-ttu-id="6a501-118">*Hora*</span><span class="sxs-lookup"><span data-stu-id="6a501-118">*Hour*</span></span>  <br/> |<span data-ttu-id="6a501-119">Expressão de inteiro especificando horas.</span><span class="sxs-lookup"><span data-stu-id="6a501-119">Integer expression specifying hours.</span></span>  <br/> |
| <span data-ttu-id="6a501-120">*Minuto*</span><span class="sxs-lookup"><span data-stu-id="6a501-120">*Minute*</span></span>  <br/> |<span data-ttu-id="6a501-121">Expressão de inteiro especificando minutos.</span><span class="sxs-lookup"><span data-stu-id="6a501-121">Integer expression specifying minutes.</span></span>  <br/> |
| <span data-ttu-id="6a501-122">*Segundo*</span><span class="sxs-lookup"><span data-stu-id="6a501-122">*Second*</span></span>  <br/> |<span data-ttu-id="6a501-123">Expressão de inteiro especificando segundos.</span><span class="sxs-lookup"><span data-stu-id="6a501-123">Integer expression specifying seconds.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="6a501-124">Comentários</span><span class="sxs-lookup"><span data-stu-id="6a501-124">Remarks</span></span>

<span data-ttu-id="6a501-125">**DateWithTimeFromParts** retorna um valor de data/hora totalmente inicializado.</span><span class="sxs-lookup"><span data-stu-id="6a501-125">**DateWithTimeFromParts** returns a fully initialized Date/Time value.</span></span> <span data-ttu-id="6a501-126">Se os argumentos não são válidos, um erro será gerado.</span><span class="sxs-lookup"><span data-stu-id="6a501-126">If the arguments are not valid, an error is raised.</span></span> <span data-ttu-id="6a501-127">Se for necessário argumentos forem nulos, Null será retornado.</span><span class="sxs-lookup"><span data-stu-id="6a501-127">If required arguments are Null, then Null is returned.</span></span> 
  

