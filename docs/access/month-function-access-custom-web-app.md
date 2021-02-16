---
title: Função Month (aplicativo Web personalizado do Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 5df43594-a434-4fb7-8109-e5cf0401ae09
description: Retorna um inteiro que representa o mês da data especificada.
ms.openlocfilehash: 0ca7059a2fd6dad1f9790ad6f4eafe7affa014dd
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33411488"
---
# <a name="month-function-access-custom-web-app"></a><span data-ttu-id="3d81e-103">Função Month (aplicativo Web personalizado do Access)</span><span class="sxs-lookup"><span data-stu-id="3d81e-103">Month Function (Access custom web app)</span></span>

<span data-ttu-id="3d81e-104">Retorna um inteiro que representa o mês da data especificada.</span><span class="sxs-lookup"><span data-stu-id="3d81e-104">Returns an integer that represents the month of the specified date.</span></span>
  
> [!NOTE]
> <span data-ttu-id="3d81e-105">O recurso de armazenamento em nuvem descrito neste artigo não tem mais suporte no Office 2013 e Office 2016, e pode resultar no seguinte erro: > *Estamos com problemas de servidor, portanto, não podemos adicionar \<serviço\> agora. Tente novamente mais tarde.*</span><span class="sxs-lookup"><span data-stu-id="3d81e-105">The cloud storage feature described in this article is no longer supported in Office 2013 and Office 2016 and may result in the following error: >  *Sorry, we're having server problems, so we can't add \<service\> right now. Please try again later.*</span></span> <span data-ttu-id="3d81e-106">> Para armazenamento em nuvem do Office Online, Office para iOS e Office para Android, você poderá pesquisar no nosso [Programa de Parceiros de Armazenamento de Nuvem do Office](https://dev.office.com/programs/officecloudstorage).</span><span class="sxs-lookup"><span data-stu-id="3d81e-106">> For cloud storage for Office Online, Office for iOS, and Office for Android, you can look into our [Office Cloud Storage Partner Program](https://dev.office.com/programs/officecloudstorage).</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="3d81e-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="3d81e-107">Syntax</span></span>

 <span data-ttu-id="3d81e-108">**Mês** (*Data*)</span><span class="sxs-lookup"><span data-stu-id="3d81e-108">**Month** (*Date*)</span></span> 
  
<span data-ttu-id="3d81e-109">A **função Month** contém o argumento a seguir.</span><span class="sxs-lookup"><span data-stu-id="3d81e-109">The **Month** function contains the following argument.</span></span> 
  
|<span data-ttu-id="3d81e-110">**Nome do argumento**</span><span class="sxs-lookup"><span data-stu-id="3d81e-110">**Argument name**</span></span>|<span data-ttu-id="3d81e-111">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="3d81e-111">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="3d81e-112">*Date*</span><span class="sxs-lookup"><span data-stu-id="3d81e-112">*Date*</span></span>  <br/> |<span data-ttu-id="3d81e-113">Uma expressão que pode ser resolvida para um valor de Data/Hora.</span><span class="sxs-lookup"><span data-stu-id="3d81e-113">An expression that can be resolved to a Date/Time value.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="3d81e-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="3d81e-114">Remarks</span></span>

 <span data-ttu-id="3d81e-115">**Month** retorna o mesmo valor que **DatePart** (mês, data).</span><span class="sxs-lookup"><span data-stu-id="3d81e-115">**Month** returns the same value as **DatePart** (month, date).</span></span> 
  
<span data-ttu-id="3d81e-116">Se  *Data*  contiver apenas uma parte de hora, o valor de retorno será 1, o mês base.</span><span class="sxs-lookup"><span data-stu-id="3d81e-116">If  *Date*  contains only a time part, the return value is 1, the base month.</span></span> 
  

