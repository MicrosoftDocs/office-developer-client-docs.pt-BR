---
title: Função FIMMÊS (aplicativo Web personalizado do Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
localization_priority: Normal
ms.assetid: df98bcca-152b-49f2-b4e1-35d68008fb8f
description: Retorna o último dia do mês antes ou o número de meses especificado.
ms.openlocfilehash: 87a837069be223fdd2f9c809d706782e0955e2aa
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32302553"
---
# <a name="eomonth-function-access-custom-web-app"></a><span data-ttu-id="47295-103">Função FIMMÊS (aplicativo Web personalizado do Access)</span><span class="sxs-lookup"><span data-stu-id="47295-103">EOMonth Function (Access custom web app)</span></span>

<span data-ttu-id="47295-104">Retorna o último dia do mês antes ou o número de meses especificado.</span><span class="sxs-lookup"><span data-stu-id="47295-104">Returns the last day of the month before or specified number of months.</span></span>
  
> [!NOTE]
> <span data-ttu-id="47295-105">O recurso de armazenamento em nuvem descrito neste artigo não tem mais suporte no Office 2013 e Office 2016, e pode resultar no seguinte erro: > *Estamos com problemas de servidor, portanto, não podemos adicionar \<serviço\> agora. Tente novamente mais tarde.*</span><span class="sxs-lookup"><span data-stu-id="47295-105">The cloud storage feature described in this article is no longer supported in Office 2013 and Office 2016 and may result in the following error: >  *Sorry, we're having server problems, so we can't add \<service\> right now. Please try again later.*</span></span> <span data-ttu-id="47295-106">> Para armazenamento em nuvem do Office Online, Office para iOS e Office para Android, você poderá pesquisar no nosso [Programa de Parceiros de Armazenamento de Nuvem do Office](https://dev.office.com/programs/officecloudstorage).</span><span class="sxs-lookup"><span data-stu-id="47295-106">> For cloud storage for Office Online, Office for iOS, and Office for Android, you can look into our [Office Cloud Storage Partner Program](https://dev.office.com/programs/officecloudstorage).</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="47295-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="47295-107">Syntax</span></span>

 <span data-ttu-id="47295-108">**FIMMÊS** (*Data*, *NumberOfMonth*)</span><span class="sxs-lookup"><span data-stu-id="47295-108">**EOMonth** (*Date*, *NumberOfMonth*)</span></span> 
  
<span data-ttu-id="47295-109">O **FIMMÊS** contém os seguintes argumentos.</span><span class="sxs-lookup"><span data-stu-id="47295-109">The **EOMonth** contains the following arguments.</span></span> 
  
|<span data-ttu-id="47295-110">**Nome do argumento**</span><span class="sxs-lookup"><span data-stu-id="47295-110">**Argument name**</span></span>|<span data-ttu-id="47295-111">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="47295-111">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="47295-112">*Date*</span><span class="sxs-lookup"><span data-stu-id="47295-112">*Date*</span></span>  <br/> |<span data-ttu-id="47295-113">A data de início no formato de data/hora ou em uma representação de texto aceita de uma data.</span><span class="sxs-lookup"><span data-stu-id="47295-113">The start date in Date/Time format, or in an accepted text representation of a date.</span></span>  <br/> |
| <span data-ttu-id="47295-114">*NumberOfMonth*</span><span class="sxs-lookup"><span data-stu-id="47295-114">*NumberOfMonth*</span></span>  <br/> |<span data-ttu-id="47295-115">Um número que representa o número de meses antes ou depois da *Data* .</span><span class="sxs-lookup"><span data-stu-id="47295-115">A number representing the number of months before or after the  *Date*  .</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="47295-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="47295-116">Remarks</span></span>

<span data-ttu-id="47295-117">Se *Data* não for uma data válida, **FIMMÊS** retornará um erro.</span><span class="sxs-lookup"><span data-stu-id="47295-117">If  *Date*  is not a valid date, **EOMonth** returns an error.</span></span> 
  
<span data-ttu-id="47295-118">Se *Date* mais *NumberOfMonth* gerar uma data inválida, **FIMMÊS** retornará um erro.</span><span class="sxs-lookup"><span data-stu-id="47295-118">If  *Date*  plus  *NumberOfMonth*  yields an invalid date, **EOMonth** returns an error.</span></span> 
  

