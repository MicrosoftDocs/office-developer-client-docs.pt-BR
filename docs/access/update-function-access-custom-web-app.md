---
title: Função de atualização (aplicativo da web personalizado do Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 8a8c52c9-81b9-4d10-b42b-e360c67bcf4e
description: Retorna se uma operação de inserção ou atualização foi tentada no campo especificado.
ms.openlocfilehash: 1685d9f44bd167571b949a34d6c7b6993e63fbc0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19765259"
---
# <a name="update-function-access-custom-web-app"></a><span data-ttu-id="98d25-103">Função de atualização (aplicativo da web personalizado do Access)</span><span class="sxs-lookup"><span data-stu-id="98d25-103">Update Function (Access custom web app)</span></span>

<span data-ttu-id="98d25-104">Retorna se uma operação de inserção ou atualização foi tentada no campo especificado.</span><span class="sxs-lookup"><span data-stu-id="98d25-104">Returns whether an INSERT or UPDATE operation was attempted on the specified field.</span></span>
  
> [!NOTE]
> <span data-ttu-id="98d25-105">O recurso de armazenamento de nuvem descrito neste artigo não é mais suportado no Office 2013 e Office 2016 e pode resultar no seguinte erro: > *Sorry, vamos ter problemas no servidor, portanto não podemos adicionar \<service\> conveniente. Tente novamente mais tarde.*</span><span class="sxs-lookup"><span data-stu-id="98d25-105">The cloud storage feature described in this article is no longer supported in Office 2013 and Office 2016 and may result in the following error: >  *Sorry, we're having server problems, so we can't add \<service\> right now. Please try again later.*</span></span> <span data-ttu-id="98d25-106">> Para armazenamento em nuvem para o Office Online, o Office para iOS e do Office para Android, você pode pesquisar em nosso [Programa de parceria de armazenamento de nuvem do Office](https://dev.office.com/programs/officecloudstorage).</span><span class="sxs-lookup"><span data-stu-id="98d25-106">> For cloud storage for Office Online, Office for iOS, and Office for Android, you can look into our [Office Cloud Storage Partner Program](https://dev.office.com/programs/officecloudstorage).</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="98d25-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="98d25-107">Syntax</span></span>

 <span data-ttu-id="98d25-108">**Atualização** (*Coluna*)</span><span class="sxs-lookup"><span data-stu-id="98d25-108">**Update** (*Column*)</span></span> 
  
<span data-ttu-id="98d25-109">A função de **atualização** contém os seguintes argumentos.</span><span class="sxs-lookup"><span data-stu-id="98d25-109">The **Update** function contains the following arguments.</span></span> 
  
|<span data-ttu-id="98d25-110">**Nome do argumento**</span><span class="sxs-lookup"><span data-stu-id="98d25-110">**Argument name**</span></span>|<span data-ttu-id="98d25-111">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="98d25-111">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="98d25-112">*Column*</span><span class="sxs-lookup"><span data-stu-id="98d25-112">*Column*</span></span>  <br/> |<span data-ttu-id="98d25-113">O nome do campo para verificar se há uma operação de inserção ou atualização.</span><span class="sxs-lookup"><span data-stu-id="98d25-113">The name of the field to check for an INSERT or UPDATE operation.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="98d25-114">Coment�rios</span><span class="sxs-lookup"><span data-stu-id="98d25-114">Remarks</span></span>

<span data-ttu-id="98d25-115">A função de **atualização** retorna TRUE, independentemente se uma tentativa INSERT ou UPDATE for bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="98d25-115">The **Update** function returns TRUE regardless of whether an INSERT or UPDATE attempt is successful.</span></span> 
  

