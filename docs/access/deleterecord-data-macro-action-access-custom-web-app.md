---
title: Ação de macro de dados DeleteRecord (aplicativo Web personalizado do Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
localization_priority: Normal
ms.assetid: f6b68a9a-e04a-476e-a407-b1779fea1953
description: Você pode usar a ação ExcluirRegistro para excluir um registro.
ms.openlocfilehash: 0e8a658b944e894e4d4014fb3d3d9a583efbee8d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32282112"
---
# <a name="deleterecord-data-macro-action-access-custom-web-app"></a><span data-ttu-id="be283-103">Ação de macro de dados DeleteRecord (aplicativo Web personalizado do Access)</span><span class="sxs-lookup"><span data-stu-id="be283-103">DeleteRecord Data Macro action (Access custom web app)</span></span>

<span data-ttu-id="be283-104">Você pode usar a ação **ExcluirRegistro** para excluir um registro.</span><span class="sxs-lookup"><span data-stu-id="be283-104">You can use the **DeleteRecord** action to delete a record.</span></span> 
  
> [!IMPORTANT]
> <span data-ttu-id="be283-p101">A Microsoft não recomenda mais criar e usar aplicativos Web do Access no SharePoint. Como alternativa, use o [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) para criar soluções de negócios sem código para a Web e dispositivos móveis.</span><span class="sxs-lookup"><span data-stu-id="be283-p101">Microsoft no longer recommends creating and using Access web apps in SharePoint. As an alternative, consider using [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) to build no-code business solutions for the web and mobile devices.</span></span> 
  
## <a name="setting"></a><span data-ttu-id="be283-107">Configuração</span><span class="sxs-lookup"><span data-stu-id="be283-107">Setting</span></span>

<span data-ttu-id="be283-108">A ação **DeleteRecord** tem os seguintes argumentos.</span><span class="sxs-lookup"><span data-stu-id="be283-108">The **DeleteRecord** action has the following arguments.</span></span> 
  
|<span data-ttu-id="be283-109">**Argumento**</span><span class="sxs-lookup"><span data-stu-id="be283-109">**Argument**</span></span>|<span data-ttu-id="be283-110">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="be283-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="be283-111">**Alias de Registro**</span><span class="sxs-lookup"><span data-stu-id="be283-111">**Record Alias**</span></span> <br/> |<span data-ttu-id="be283-112">Uma cadeia de caracteres que identifica o registro a ser excluído.</span><span class="sxs-lookup"><span data-stu-id="be283-112">A string that identifies the record to delete.</span></span> <span data-ttu-id="be283-113">Se o argumento *alias* não for especificado, o registro atual será excluído.</span><span class="sxs-lookup"><span data-stu-id="be283-113">If the  *Alias*  argument is not specified, then the current record is deleted.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="be283-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="be283-114">Remarks</span></span>

<span data-ttu-id="be283-115">Você pode usar a variável local **IdentidadedeRegistroCriadapelaÚltimaVez** para executá-la com o último registro criado em um bloco de dados **CriarRegistro**.</span><span class="sxs-lookup"><span data-stu-id="be283-115">You can use the **LastCreateRecordIdentity** local variable to work with last record created in a **CreateRecord** data block.</span></span> <span data-ttu-id="be283-116">Por exemplo, use a sintaxe a seguir para fazer referência ao registro criado mais recentemente:</span><span class="sxs-lookup"><span data-stu-id="be283-116">For example, use the following syntax to refer to the most recently created record:</span></span> 
  
`[LastCreateRecordIdentity]`


