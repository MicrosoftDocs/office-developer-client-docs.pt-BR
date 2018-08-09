---
title: Função DateFromParts (aplicativo da web personalizado do Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
localization_priority: Normal
ms.assetid: 4fa49d5f-12ea-4d14-9a03-28418f01746c
description: Retorna um valor de data para o ano especificado, mês e dia.
ms.openlocfilehash: 5a2ff76d99076cf9f53b0dce8c5019f38d910f58
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19765032"
---
# <a name="datefromparts-function-access-custom-web-app"></a><span data-ttu-id="f48ca-103">Função DateFromParts (aplicativo da web personalizado do Access)</span><span class="sxs-lookup"><span data-stu-id="f48ca-103">DateFromParts function (Access custom web app)</span></span>

<span data-ttu-id="f48ca-104">Retorna um valor de data para o ano especificado, mês e dia.</span><span class="sxs-lookup"><span data-stu-id="f48ca-104">Returns a date value for the specified year, month, and day.</span></span>
  
> [!NOTE]
> <span data-ttu-id="f48ca-105">O recurso de armazenamento de nuvem descrito neste artigo não é mais suportado no Office 2013 e Office 2016 e pode resultar no seguinte erro: > *Sorry, vamos ter problemas no servidor, portanto não podemos adicionar \<service\> conveniente. Tente novamente mais tarde.*</span><span class="sxs-lookup"><span data-stu-id="f48ca-105">The cloud storage feature described in this article is no longer supported in Office 2013 and Office 2016 and may result in the following error: >  *Sorry, we're having server problems, so we can't add \<service\> right now. Please try again later.*</span></span> <span data-ttu-id="f48ca-106">> Para armazenamento em nuvem para o Office Online, o Office para iOS e do Office para Android, você pode pesquisar em nosso [Programa de parceria de armazenamento de nuvem do Office](https://dev.office.com/programs/officecloudstorage).</span><span class="sxs-lookup"><span data-stu-id="f48ca-106">> For cloud storage for Office Online, Office for iOS, and Office for Android, you can look into our [Office Cloud Storage Partner Program](https://dev.office.com/programs/officecloudstorage).</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="f48ca-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f48ca-107">Syntax</span></span>

<span data-ttu-id="f48ca-108">**DateFromParts** (*Ano*, *mês*, *dia*)</span><span class="sxs-lookup"><span data-stu-id="f48ca-108">**DateFromParts** (*Year*, *Month*, *Day*)</span></span> 
  
<span data-ttu-id="f48ca-109">A função **DateFromParts** contém os seguintes argumentos.</span><span class="sxs-lookup"><span data-stu-id="f48ca-109">The **DateFromParts** function contains the following arguments.</span></span> 
  
|<span data-ttu-id="f48ca-110">**Nome do argumento**</span><span class="sxs-lookup"><span data-stu-id="f48ca-110">**Argument name**</span></span>|<span data-ttu-id="f48ca-111">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="f48ca-111">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="f48ca-112">*Ano*</span><span class="sxs-lookup"><span data-stu-id="f48ca-112">*Year*</span></span>  <br/> |<span data-ttu-id="f48ca-113">Expressão de inteiro especificando um ano.</span><span class="sxs-lookup"><span data-stu-id="f48ca-113">Integer expression specifying a year.</span></span>  <br/> |
| <span data-ttu-id="f48ca-114">*Month*</span><span class="sxs-lookup"><span data-stu-id="f48ca-114">*Month*</span></span>  <br/> |<span data-ttu-id="f48ca-115">Expressão de inteiro especificando um mês, de 1 a 12.</span><span class="sxs-lookup"><span data-stu-id="f48ca-115">Integer expression specifying a month, from 1 to 12.</span></span>  <br/> |
| <span data-ttu-id="f48ca-116">*Dia*</span><span class="sxs-lookup"><span data-stu-id="f48ca-116">*Day*</span></span>  <br/> |<span data-ttu-id="f48ca-117">Expressão de inteiro especificando um dia.</span><span class="sxs-lookup"><span data-stu-id="f48ca-117">Integer expression specifying a day.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="f48ca-118">Comentários</span><span class="sxs-lookup"><span data-stu-id="f48ca-118">Remarks</span></span>

<span data-ttu-id="f48ca-119">**DateFromParts** retorna um valor de data com a parte da data definida como a parte de hora definido como o padrão e dia, mês e ano especificado.</span><span class="sxs-lookup"><span data-stu-id="f48ca-119">**DateFromParts** returns a date value with the date portion set to the specified year, month and day, and the time portion set to the default.</span></span> <span data-ttu-id="f48ca-120">Se os argumentos não são válidos, um erro é gerado.</span><span class="sxs-lookup"><span data-stu-id="f48ca-120">If the arguments are not valid, then an error is raised.</span></span> <span data-ttu-id="f48ca-121">Se for necessário argumentos são nulos, nulo será retornado.</span><span class="sxs-lookup"><span data-stu-id="f48ca-121">If required arguments are null, then NULL is returned.</span></span> 
  
## <a name="example"></a><span data-ttu-id="f48ca-122">Exemplo</span><span class="sxs-lookup"><span data-stu-id="f48ca-122">Example</span></span>

<span data-ttu-id="f48ca-123">A expressão a seguir utiliza a função **DateFromParts** para calcular o primeiro dia do mês atual.</span><span class="sxs-lookup"><span data-stu-id="f48ca-123">The following expression uses the **DateFromParts** function to calculate the first day of the current month.</span></span> 
  
`DateFromParts(Year(Today()),Month(Today()),1)`



