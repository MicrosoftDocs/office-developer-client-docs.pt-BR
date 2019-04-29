---
title: Função TimeFromParts (aplicativo Web personalizado do Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 7f631b7e-6e3c-46dc-a05f-6a07f9a91268
description: Retorna um valor de tempo com base em partes especificadas.
ms.openlocfilehash: 8e2105140056bc65e9af0a6eda6e40fc44caed1a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33417991"
---
# <a name="timefromparts-function-access-custom-web-app"></a><span data-ttu-id="11c09-103">Função TimeFromParts (aplicativo Web personalizado do Access)</span><span class="sxs-lookup"><span data-stu-id="11c09-103">TimeFromParts Function (Access custom web app)</span></span>

<span data-ttu-id="11c09-104">Retorna um valor de tempo com base em partes especificadas.</span><span class="sxs-lookup"><span data-stu-id="11c09-104">Returns a time value based on specified parts.</span></span>
  
> [!NOTE]
> <span data-ttu-id="11c09-105">O recurso de armazenamento em nuvem descrito neste artigo não tem mais suporte no Office 2013 e Office 2016, e pode resultar no seguinte erro: > *Estamos com problemas de servidor, portanto, não podemos adicionar \<serviço\> agora. Tente novamente mais tarde.*</span><span class="sxs-lookup"><span data-stu-id="11c09-105">The cloud storage feature described in this article is no longer supported in Office 2013 and Office 2016 and may result in the following error: >  *Sorry, we're having server problems, so we can't add \<service\> right now. Please try again later.*</span></span> <span data-ttu-id="11c09-106">> Para armazenamento em nuvem do Office Online, Office para iOS e Office para Android, você poderá pesquisar no nosso [Programa de Parceiros de Armazenamento de Nuvem do Office](https://dev.office.com/programs/officecloudstorage).</span><span class="sxs-lookup"><span data-stu-id="11c09-106">> For cloud storage for Office Online, Office for iOS, and Office for Android, you can look into our [Office Cloud Storage Partner Program](https://dev.office.com/programs/officecloudstorage).</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="11c09-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="11c09-107">Syntax</span></span>

 <span data-ttu-id="11c09-108">**TimeFromParts** (*Hora*, *minuto*, *segundo*)</span><span class="sxs-lookup"><span data-stu-id="11c09-108">**TimeFromParts** (*Hour*, *Minute*, *Second*)</span></span> 
  
<span data-ttu-id="11c09-109">A função **TimeFromParts** contém os seguintes argumentos.</span><span class="sxs-lookup"><span data-stu-id="11c09-109">The **TimeFromParts** function contains the following arguments.</span></span> 
  
|<span data-ttu-id="11c09-110">**Nome do argumento**</span><span class="sxs-lookup"><span data-stu-id="11c09-110">**Argument name**</span></span>|<span data-ttu-id="11c09-111">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="11c09-111">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="11c09-112">*Hour*</span><span class="sxs-lookup"><span data-stu-id="11c09-112">*Hour*</span></span>  <br/> |<span data-ttu-id="11c09-113">Expressão de inteiro especificando horas.</span><span class="sxs-lookup"><span data-stu-id="11c09-113">Integer expression specifying hours.</span></span>  <br/> |
| <span data-ttu-id="11c09-114">*Minute*</span><span class="sxs-lookup"><span data-stu-id="11c09-114">*Minute*</span></span>  <br/> |<span data-ttu-id="11c09-115">Expressão de inteiro especificando minutos.</span><span class="sxs-lookup"><span data-stu-id="11c09-115">Integer expression specifying minutes.</span></span>  <br/> |
| <span data-ttu-id="11c09-116">*Second*</span><span class="sxs-lookup"><span data-stu-id="11c09-116">*Second*</span></span>  <br/> |<span data-ttu-id="11c09-117">Expressão de inteiro especificando segundos.</span><span class="sxs-lookup"><span data-stu-id="11c09-117">Integer expression specifying seconds.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="11c09-118">Confira também</span><span class="sxs-lookup"><span data-stu-id="11c09-118">See also</span></span>

 <span data-ttu-id="11c09-119">**TimeFromParts** retorna um valor de hora totalmente inicializado.</span><span class="sxs-lookup"><span data-stu-id="11c09-119">**TimeFromParts** returns a fully initialized time value.</span></span> <span data-ttu-id="11c09-120">Se os argumentos forem inválidos, um erro será gerado.</span><span class="sxs-lookup"><span data-stu-id="11c09-120">If the arguments are invalid, then an error is raised.</span></span> <span data-ttu-id="11c09-121">Se qualquer um dos parâmetros for NULL, NULL será retornado.</span><span class="sxs-lookup"><span data-stu-id="11c09-121">If any of the parameters are null, null is returned.</span></span> 
  

