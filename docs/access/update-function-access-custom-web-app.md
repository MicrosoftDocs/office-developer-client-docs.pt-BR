---
title: Função Update (aplicativo Web personalizado do Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 8a8c52c9-81b9-4d10-b42b-e360c67bcf4e
description: Retorna se uma operação de inserção ou atualização foi tentada no campo especificado.
ms.openlocfilehash: 20e1b87be857f302f36244a6733625dc477da912
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33410914"
---
# <a name="update-function-access-custom-web-app"></a><span data-ttu-id="b2d2f-103">Função Update (aplicativo Web personalizado do Access)</span><span class="sxs-lookup"><span data-stu-id="b2d2f-103">Update Function (Access custom web app)</span></span>

<span data-ttu-id="b2d2f-104">Retorna se uma operação de inserção ou atualização foi tentada no campo especificado.</span><span class="sxs-lookup"><span data-stu-id="b2d2f-104">Returns whether an INSERT or UPDATE operation was attempted on the specified field.</span></span>
  
> [!NOTE]
> <span data-ttu-id="b2d2f-105">O recurso de armazenamento em nuvem descrito neste artigo não tem mais suporte no Office 2013 e Office 2016, e pode resultar no seguinte erro: > *Estamos com problemas de servidor, portanto, não podemos adicionar \<serviço\> agora. Tente novamente mais tarde.*</span><span class="sxs-lookup"><span data-stu-id="b2d2f-105">The cloud storage feature described in this article is no longer supported in Office 2013 and Office 2016 and may result in the following error: >  *Sorry, we're having server problems, so we can't add \<service\> right now. Please try again later.*</span></span> <span data-ttu-id="b2d2f-106">> Para armazenamento em nuvem do Office Online, Office para iOS e Office para Android, você poderá pesquisar no nosso [Programa de Parceiros de Armazenamento de Nuvem do Office](https://dev.office.com/programs/officecloudstorage).</span><span class="sxs-lookup"><span data-stu-id="b2d2f-106">> For cloud storage for Office Online, Office for iOS, and Office for Android, you can look into our [Office Cloud Storage Partner Program](https://dev.office.com/programs/officecloudstorage).</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="b2d2f-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b2d2f-107">Syntax</span></span>

 <span data-ttu-id="b2d2f-108">**Atualização** do (*Coluna*)</span><span class="sxs-lookup"><span data-stu-id="b2d2f-108">**Update** (*Column*)</span></span> 
  
<span data-ttu-id="b2d2f-109">A função **Update** contém os seguintes argumentos.</span><span class="sxs-lookup"><span data-stu-id="b2d2f-109">The **Update** function contains the following arguments.</span></span> 
  
|<span data-ttu-id="b2d2f-110">**Nome do argumento**</span><span class="sxs-lookup"><span data-stu-id="b2d2f-110">**Argument name**</span></span>|<span data-ttu-id="b2d2f-111">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="b2d2f-111">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="b2d2f-112">*Column*</span><span class="sxs-lookup"><span data-stu-id="b2d2f-112">*Column*</span></span>  <br/> |<span data-ttu-id="b2d2f-113">O nome do campo a ser verificado para uma operação de inserção ou atualização.</span><span class="sxs-lookup"><span data-stu-id="b2d2f-113">The name of the field to check for an INSERT or UPDATE operation.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="b2d2f-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="b2d2f-114">Remarks</span></span>

<span data-ttu-id="b2d2f-115">A função **Update** retorna true independentemente de uma tentativa de inserção ou atualização ter sido bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="b2d2f-115">The **Update** function returns TRUE regardless of whether an INSERT or UPDATE attempt is successful.</span></span> 
  

