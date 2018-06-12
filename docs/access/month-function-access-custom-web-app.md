---
title: Função Month (aplicativo da web personalizado do Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 5df43594-a434-4fb7-8109-e5cf0401ae09
description: Retorna um inteiro que representa o mês da data especificada.
ms.openlocfilehash: 5e4a583a5a299456e57b90d7cef41a32b0a6ffba
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19765205"
---
# <a name="month-function-access-custom-web-app"></a><span data-ttu-id="864d8-103">Função Month (aplicativo da web personalizado do Access)</span><span class="sxs-lookup"><span data-stu-id="864d8-103">Month Function (Access custom web app)</span></span>

<span data-ttu-id="864d8-104">Retorna um inteiro que representa o mês da data especificada.</span><span class="sxs-lookup"><span data-stu-id="864d8-104">Returns an integer that represents the month of the specified date.</span></span>
  
> [!NOTE]
> <span data-ttu-id="864d8-105">O recurso de armazenamento de nuvem descrito neste artigo não é mais suportado no Office 2013 e Office 2016 e pode resultar no seguinte erro: > *Sorry, vamos ter problemas no servidor, portanto não podemos adicionar \<service\> conveniente. Tente novamente mais tarde.*</span><span class="sxs-lookup"><span data-stu-id="864d8-105">The cloud storage feature described in this article is no longer supported in Office 2013 and Office 2016 and may result in the following error: >  *Sorry, we're having server problems, so we can't add \<service\> right now. Please try again later.*</span></span> <span data-ttu-id="864d8-106">> Para armazenamento em nuvem para o Office Online, o Office para iOS e do Office para Android, você pode pesquisar em nosso [Programa de parceria de armazenamento de nuvem do Office](https://dev.office.com/programs/officecloudstorage).</span><span class="sxs-lookup"><span data-stu-id="864d8-106">> For cloud storage for Office Online, Office for iOS, and Office for Android, you can look into our [Office Cloud Storage Partner Program](https://dev.office.com/programs/officecloudstorage).</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="864d8-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="864d8-107">Syntax</span></span>

 <span data-ttu-id="864d8-108">**Mês** (*Data*)</span><span class="sxs-lookup"><span data-stu-id="864d8-108">**Month** (*Date*)</span></span> 
  
<span data-ttu-id="864d8-109">A função **Month** contém os seguintes argumentos.</span><span class="sxs-lookup"><span data-stu-id="864d8-109">The **Month** function contains the following argument.</span></span> 
  
|<span data-ttu-id="864d8-110">**Nome do argumento**</span><span class="sxs-lookup"><span data-stu-id="864d8-110">**Argument name**</span></span>|<span data-ttu-id="864d8-111">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="864d8-111">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="864d8-112">*Date*</span><span class="sxs-lookup"><span data-stu-id="864d8-112">*Date*</span></span>  <br/> |<span data-ttu-id="864d8-113">Uma expressão que pode ser resolvida como um valor de data/hora.</span><span class="sxs-lookup"><span data-stu-id="864d8-113">An expression that can be resolved to a Date/Time value.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="864d8-114">Coment�rios</span><span class="sxs-lookup"><span data-stu-id="864d8-114">Remarks</span></span>

 <span data-ttu-id="864d8-115">**Mês** retorna o mesmo valor que **DatePart** (mês, data).</span><span class="sxs-lookup"><span data-stu-id="864d8-115">**Month** returns the same value as **DatePart** (month, date).</span></span> 
  
<span data-ttu-id="864d8-116">Se *Data* contiver apenas uma parte do tempo, o valor de retorno é 1, o mês de base.</span><span class="sxs-lookup"><span data-stu-id="864d8-116">If  *Date*  contains only a time part, the return value is 1, the base month.</span></span> 
  

