---
title: Função TimeFromParts (aplicativo da web personalizado do Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 7f631b7e-6e3c-46dc-a05f-6a07f9a91268
description: Retorna um valor de tempo com base em partes especificadas.
ms.openlocfilehash: 55a4d1c31fdd2248e3e154d83e803d9f5a5ebb06
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19765235"
---
# <a name="timefromparts-function-access-custom-web-app"></a><span data-ttu-id="cb244-103">Função TimeFromParts (aplicativo da web personalizado do Access)</span><span class="sxs-lookup"><span data-stu-id="cb244-103">TimeFromParts Function (Access custom web app)</span></span>

<span data-ttu-id="cb244-104">Retorna um valor de tempo com base em partes especificadas.</span><span class="sxs-lookup"><span data-stu-id="cb244-104">Returns a time value based on specified parts.</span></span>
  
> [!NOTE]
> <span data-ttu-id="cb244-105">O recurso de armazenamento de nuvem descrito neste artigo não é mais suportado no Office 2013 e Office 2016 e pode resultar no seguinte erro: > *Sorry, vamos ter problemas no servidor, portanto não podemos adicionar \<service\> conveniente. Tente novamente mais tarde.*</span><span class="sxs-lookup"><span data-stu-id="cb244-105">The cloud storage feature described in this article is no longer supported in Office 2013 and Office 2016 and may result in the following error: >  *Sorry, we're having server problems, so we can't add \<service\> right now. Please try again later.*</span></span> <span data-ttu-id="cb244-106">> Para armazenamento em nuvem para o Office Online, o Office para iOS e do Office para Android, você pode pesquisar em nosso [Programa de parceria de armazenamento de nuvem do Office](https://dev.office.com/programs/officecloudstorage).</span><span class="sxs-lookup"><span data-stu-id="cb244-106">> For cloud storage for Office Online, Office for iOS, and Office for Android, you can look into our [Office Cloud Storage Partner Program](https://dev.office.com/programs/officecloudstorage).</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="cb244-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="cb244-107">Syntax</span></span>

 <span data-ttu-id="cb244-108">**TimeFromParts** (*Hora*, *minuto*, *segundo*)</span><span class="sxs-lookup"><span data-stu-id="cb244-108">**TimeFromParts** (*Hour*, *Minute*, *Second*)</span></span> 
  
<span data-ttu-id="cb244-109">A função **TimeFromParts** contém os seguintes argumentos.</span><span class="sxs-lookup"><span data-stu-id="cb244-109">The **TimeFromParts** function contains the following arguments.</span></span> 
  
|<span data-ttu-id="cb244-110">**Nome do argumento**</span><span class="sxs-lookup"><span data-stu-id="cb244-110">**Argument name**</span></span>|<span data-ttu-id="cb244-111">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="cb244-111">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="cb244-112">*Hora*</span><span class="sxs-lookup"><span data-stu-id="cb244-112">*Hour*</span></span>  <br/> |<span data-ttu-id="cb244-113">Expressão de inteiro especificando horas.</span><span class="sxs-lookup"><span data-stu-id="cb244-113">Integer expression specifying hours.</span></span>  <br/> |
| <span data-ttu-id="cb244-114">*Minuto*</span><span class="sxs-lookup"><span data-stu-id="cb244-114">*Minute*</span></span>  <br/> |<span data-ttu-id="cb244-115">Expressão de inteiro especificando minutos.</span><span class="sxs-lookup"><span data-stu-id="cb244-115">Integer expression specifying minutes.</span></span>  <br/> |
| <span data-ttu-id="cb244-116">*Segundo*</span><span class="sxs-lookup"><span data-stu-id="cb244-116">*Second*</span></span>  <br/> |<span data-ttu-id="cb244-117">Expressão de inteiro especificando segundos.</span><span class="sxs-lookup"><span data-stu-id="cb244-117">Integer expression specifying seconds.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="cb244-118">Confira também</span><span class="sxs-lookup"><span data-stu-id="cb244-118">See also</span></span>

 <span data-ttu-id="cb244-119">**TimeFromParts** retorna um valor de tempo totalmente inicializado.</span><span class="sxs-lookup"><span data-stu-id="cb244-119">**TimeFromParts** returns a fully initialized time value.</span></span> <span data-ttu-id="cb244-120">Se os argumentos são inválidos, um erro é gerado.</span><span class="sxs-lookup"><span data-stu-id="cb244-120">If the arguments are invalid, then an error is raised.</span></span> <span data-ttu-id="cb244-121">Se qualquer um dos parâmetros forem nulo, nulo será retornado.</span><span class="sxs-lookup"><span data-stu-id="cb244-121">If any of the parameters are null, null is returned.</span></span> 
  

