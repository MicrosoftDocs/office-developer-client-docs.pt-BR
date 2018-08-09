---
title: Função FIMMÊS (aplicativo da web personalizado do Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
localization_priority: Normal
ms.assetid: df98bcca-152b-49f2-b4e1-35d68008fb8f
description: Retorna o último dia do mês antes ou do número especificado de meses.
ms.openlocfilehash: cee42c4e5cb3a24b2e702673238ac9ee09bc7372
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19765051"
---
# <a name="eomonth-function-access-custom-web-app"></a><span data-ttu-id="cf62e-103">Função FIMMÊS (aplicativo da web personalizado do Access)</span><span class="sxs-lookup"><span data-stu-id="cf62e-103">EOMonth Function (Access custom web app)</span></span>

<span data-ttu-id="cf62e-104">Retorna o último dia do mês antes ou do número especificado de meses.</span><span class="sxs-lookup"><span data-stu-id="cf62e-104">Returns the last day of the month before or specified number of months.</span></span>
  
> [!NOTE]
> <span data-ttu-id="cf62e-105">O recurso de armazenamento de nuvem descrito neste artigo não é mais suportado no Office 2013 e Office 2016 e pode resultar no seguinte erro: > *Sorry, vamos ter problemas no servidor, portanto não podemos adicionar \<service\> conveniente. Tente novamente mais tarde.*</span><span class="sxs-lookup"><span data-stu-id="cf62e-105">The cloud storage feature described in this article is no longer supported in Office 2013 and Office 2016 and may result in the following error: >  *Sorry, we're having server problems, so we can't add \<service\> right now. Please try again later.*</span></span> <span data-ttu-id="cf62e-106">> Para armazenamento em nuvem para o Office Online, o Office para iOS e do Office para Android, você pode pesquisar em nosso [Programa de parceria de armazenamento de nuvem do Office](https://dev.office.com/programs/officecloudstorage).</span><span class="sxs-lookup"><span data-stu-id="cf62e-106">> For cloud storage for Office Online, Office for iOS, and Office for Android, you can look into our [Office Cloud Storage Partner Program](https://dev.office.com/programs/officecloudstorage).</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="cf62e-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="cf62e-107">Syntax</span></span>

 <span data-ttu-id="cf62e-108">**FIMMÊS** (*Data*, *NumberOfMonth*)</span><span class="sxs-lookup"><span data-stu-id="cf62e-108">**EOMonth** (*Date*, *NumberOfMonth*)</span></span> 
  
<span data-ttu-id="cf62e-109">O **FIMMÊS** contém os seguintes argumentos.</span><span class="sxs-lookup"><span data-stu-id="cf62e-109">The **EOMonth** contains the following arguments.</span></span> 
  
|<span data-ttu-id="cf62e-110">**Nome do argumento**</span><span class="sxs-lookup"><span data-stu-id="cf62e-110">**Argument name**</span></span>|<span data-ttu-id="cf62e-111">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="cf62e-111">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="cf62e-112">*Date*</span><span class="sxs-lookup"><span data-stu-id="cf62e-112">*Date*</span></span>  <br/> |<span data-ttu-id="cf62e-113">A data de início em formato de data/hora, ou em uma representação em texto aceitos de uma data.</span><span class="sxs-lookup"><span data-stu-id="cf62e-113">The start date in Date/Time format, or in an accepted text representation of a date.</span></span>  <br/> |
| <span data-ttu-id="cf62e-114">*NumberOfMonth*</span><span class="sxs-lookup"><span data-stu-id="cf62e-114">*NumberOfMonth*</span></span>  <br/> |<span data-ttu-id="cf62e-115">Um número que representa o número de meses antes ou depois da *Data* .</span><span class="sxs-lookup"><span data-stu-id="cf62e-115">A number representing the number of months before or after the  *Date*  .</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="cf62e-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="cf62e-116">Remarks</span></span>

<span data-ttu-id="cf62e-117">Se *Data* não for uma data válida, **FIMMÊS** retornará um erro.</span><span class="sxs-lookup"><span data-stu-id="cf62e-117">If  *Date*  is not a valid date, **EOMonth** returns an error.</span></span> 
  
<span data-ttu-id="cf62e-118">Se a *Data* mais *NumberOfMonth* gerarem uma data inválida, **FIMMÊS** retornará um erro.</span><span class="sxs-lookup"><span data-stu-id="cf62e-118">If  *Date*  plus  *NumberOfMonth*  yields an invalid date, **EOMonth** returns an error.</span></span> 
  

