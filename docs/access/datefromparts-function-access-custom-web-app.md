---
title: Função DateFromParts (aplicativo Web personalizado do Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
localization_priority: Normal
ms.assetid: 4fa49d5f-12ea-4d14-9a03-28418f01746c
description: Retorna um valor de data para o ano, mês e dia especificados.
ms.openlocfilehash: 7d47fe93d1990365f1db5885a3ea8fc056aabb9f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33423220"
---
# <a name="datefromparts-function-access-custom-web-app"></a><span data-ttu-id="20ec5-103">Função DateFromParts (aplicativo Web personalizado do Access)</span><span class="sxs-lookup"><span data-stu-id="20ec5-103">DateFromParts function (Access custom web app)</span></span>

<span data-ttu-id="20ec5-104">Retorna um valor de data para o ano, mês e dia especificados.</span><span class="sxs-lookup"><span data-stu-id="20ec5-104">Returns a date value for the specified year, month, and day.</span></span>
  
> [!NOTE]
> <span data-ttu-id="20ec5-105">O recurso de armazenamento em nuvem descrito neste artigo não tem mais suporte no Office 2013 e Office 2016, e pode resultar no seguinte erro: > *Estamos com problemas de servidor, portanto, não podemos adicionar \<serviço\> agora. Tente novamente mais tarde.*</span><span class="sxs-lookup"><span data-stu-id="20ec5-105">The cloud storage feature described in this article is no longer supported in Office 2013 and Office 2016 and may result in the following error: >  *Sorry, we're having server problems, so we can't add \<service\> right now. Please try again later.*</span></span> <span data-ttu-id="20ec5-106">> Para armazenamento em nuvem do Office Online, Office para iOS e Office para Android, você poderá pesquisar no nosso [Programa de Parceiros de Armazenamento de Nuvem do Office](https://dev.office.com/programs/officecloudstorage).</span><span class="sxs-lookup"><span data-stu-id="20ec5-106">> For cloud storage for Office Online, Office for iOS, and Office for Android, you can look into our [Office Cloud Storage Partner Program](https://dev.office.com/programs/officecloudstorage).</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="20ec5-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="20ec5-107">Syntax</span></span>

<span data-ttu-id="20ec5-108">**DateFromParts** (*Ano*, *mês*, *dia*)</span><span class="sxs-lookup"><span data-stu-id="20ec5-108">**DateFromParts** (*Year*, *Month*, *Day*)</span></span> 
  
<span data-ttu-id="20ec5-109">A função **DateFromParts** contém os seguintes argumentos.</span><span class="sxs-lookup"><span data-stu-id="20ec5-109">The **DateFromParts** function contains the following arguments.</span></span> 
  
|<span data-ttu-id="20ec5-110">**Nome do argumento**</span><span class="sxs-lookup"><span data-stu-id="20ec5-110">**Argument name**</span></span>|<span data-ttu-id="20ec5-111">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="20ec5-111">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="20ec5-112">*Year*</span><span class="sxs-lookup"><span data-stu-id="20ec5-112">*Year*</span></span>  <br/> |<span data-ttu-id="20ec5-113">Expressão de inteiro que especifica um ano.</span><span class="sxs-lookup"><span data-stu-id="20ec5-113">Integer expression specifying a year.</span></span>  <br/> |
| <span data-ttu-id="20ec5-114">*Month*</span><span class="sxs-lookup"><span data-stu-id="20ec5-114">*Month*</span></span>  <br/> |<span data-ttu-id="20ec5-115">Expressão de inteiro que especifica um mês, de 1 a 12.</span><span class="sxs-lookup"><span data-stu-id="20ec5-115">Integer expression specifying a month, from 1 to 12.</span></span>  <br/> |
| <span data-ttu-id="20ec5-116">*Day*</span><span class="sxs-lookup"><span data-stu-id="20ec5-116">*Day*</span></span>  <br/> |<span data-ttu-id="20ec5-117">Expressão de inteiro que especifica um dia.</span><span class="sxs-lookup"><span data-stu-id="20ec5-117">Integer expression specifying a day.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="20ec5-118">Comentários</span><span class="sxs-lookup"><span data-stu-id="20ec5-118">Remarks</span></span>

<span data-ttu-id="20ec5-119">**DateFromParts** retorna um valor de data com a parte de data definida para o ano, mês e dia especificados, e a parte de hora definida como padrão.</span><span class="sxs-lookup"><span data-stu-id="20ec5-119">**DateFromParts** returns a date value with the date portion set to the specified year, month and day, and the time portion set to the default.</span></span> <span data-ttu-id="20ec5-120">Se os argumentos não forem válidos, ocorrerá um erro.</span><span class="sxs-lookup"><span data-stu-id="20ec5-120">If the arguments are not valid, then an error is raised.</span></span> <span data-ttu-id="20ec5-121">Se os argumentos necessários forem nulos, NULL será retornado.</span><span class="sxs-lookup"><span data-stu-id="20ec5-121">If required arguments are null, then NULL is returned.</span></span> 
  
## <a name="example"></a><span data-ttu-id="20ec5-122">Exemplo</span><span class="sxs-lookup"><span data-stu-id="20ec5-122">Example</span></span>

<span data-ttu-id="20ec5-123">A expressão a seguir usa a função **DateFromParts** para calcular o primeiro dia do mês atual.</span><span class="sxs-lookup"><span data-stu-id="20ec5-123">The following expression uses the **DateFromParts** function to calculate the first day of the current month.</span></span> 
  
`DateFromParts(Year(Today()),Month(Today()),1)`



