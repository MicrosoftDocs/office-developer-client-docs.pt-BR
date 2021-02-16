---
title: Ação de macro AbrirPopup (aplicativo Web personalizado do Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 850de802-e417-4884-8d14-571de52aa391
description: Abre o exibição especificado em uma janela pop-up.
ms.openlocfilehash: 2a8b67fcbf31c42f13b36f06d14d9d046be68c68
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33427385"
---
# <a name="openpopup-macro-action-access-custom-web-app"></a><span data-ttu-id="9cc35-103">Ação de macro AbrirPopup (aplicativo Web personalizado do Access)</span><span class="sxs-lookup"><span data-stu-id="9cc35-103">OpenPopup Macro Action (Access custom web app)</span></span>

<span data-ttu-id="9cc35-104">Abre o exibição especificado em uma janela pop-up.</span><span class="sxs-lookup"><span data-stu-id="9cc35-104">Opens the specified view in a popup window.</span></span>
  
> [!IMPORTANT]
> <span data-ttu-id="9cc35-p101">A Microsoft não recomenda mais criar e usar aplicativos Web do Access no SharePoint. Como alternativa, use o [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) para criar soluções de negócios sem código para a Web e dispositivos móveis.</span><span class="sxs-lookup"><span data-stu-id="9cc35-p101">Microsoft no longer recommends creating and using Access web apps in SharePoint. As an alternative, consider using [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) to build no-code business solutions for the web and mobile devices.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="9cc35-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="9cc35-107">Syntax</span></span>

 <span data-ttu-id="9cc35-108">**OpenPopup** (*View*, *Where=*, *Order By*)</span><span class="sxs-lookup"><span data-stu-id="9cc35-108">**OpenPopup** (*View*, *Where=*, *Order By*)</span></span> 
  
<span data-ttu-id="9cc35-109">A **ação AbrirPopup** contém os seguintes argumentos.</span><span class="sxs-lookup"><span data-stu-id="9cc35-109">The **OpenPopup** action contains the following arguments.</span></span> 
  
|<span data-ttu-id="9cc35-110">**Nome do argumento**</span><span class="sxs-lookup"><span data-stu-id="9cc35-110">**Argument name**</span></span>|<span data-ttu-id="9cc35-111">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="9cc35-111">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="9cc35-112">*View*</span><span class="sxs-lookup"><span data-stu-id="9cc35-112">*View*</span></span>  <br/> |<span data-ttu-id="9cc35-113">O nome do modo de exibição que será aberto.</span><span class="sxs-lookup"><span data-stu-id="9cc35-113">The name of the view to open.</span></span>  <br/> |
| <span data-ttu-id="9cc35-114">*Where=*</span><span class="sxs-lookup"><span data-stu-id="9cc35-114">*Where=*</span></span>  <br/> |<span data-ttu-id="9cc35-115">Uma cláusula SQL WHERE válida (sem a palavra WHERE) que restringe os registros no exibição.</span><span class="sxs-lookup"><span data-stu-id="9cc35-115">A valid SQL WHERE clause (without the word WHERE) that restricts the records in the view.</span></span>  <br/> |
| <span data-ttu-id="9cc35-116">*Classificado Por*</span><span class="sxs-lookup"><span data-stu-id="9cc35-116">*Order By*</span></span>  <br/> |<span data-ttu-id="9cc35-117">Uma expressão de cadeia de caracteres que inclui o nome do(s) campo(s) no(s) qual(is) serão classificados os registros e as palavras-chave CRESC ou DECRESC opcionais.</span><span class="sxs-lookup"><span data-stu-id="9cc35-117">A string expression that includes the name of the field or fields on which to sort records and the optional ASC or DESC keywords.</span></span> <span data-ttu-id="9cc35-118">Por padrão, esse argumento fica em branco.</span><span class="sxs-lookup"><span data-stu-id="9cc35-118">By default, this argument is blank.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="9cc35-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="9cc35-119">Remarks</span></span>

<span data-ttu-id="9cc35-120">A macro atual termina depois que **a ação AbrirPopup** é processada.</span><span class="sxs-lookup"><span data-stu-id="9cc35-120">The current macro ends once the **OpenPopup** action is processed.</span></span> 
  
<span data-ttu-id="9cc35-121">Qualquer classificação ou filtragem aplicada pelo usuário é limpa quando a **ação AbrirPopup** é chamada.</span><span class="sxs-lookup"><span data-stu-id="9cc35-121">Any sorting or filtering applied by the user is cleared when the **OpenPopup** action is called.</span></span> 
  
<span data-ttu-id="9cc35-122">O  *argumento OrderBy*  é o nome do campo ou dos campos nos quais você deseja classificar registros.</span><span class="sxs-lookup"><span data-stu-id="9cc35-122">The  *OrderBy*  argument is the name of the field or fields on which you want to sort records.</span></span> <span data-ttu-id="9cc35-123">Quando você usa mais de um nome de campo, separe-os com uma vírgula (,).</span><span class="sxs-lookup"><span data-stu-id="9cc35-123">When you use more than one field name, separate the names with a comma (,).</span></span> 
  
<span data-ttu-id="9cc35-124">Quando você definir o  *argumento OrderBy,*  os registros serão organizados por padrão em ordem crescente.</span><span class="sxs-lookup"><span data-stu-id="9cc35-124">When you set the  *OrderBy*  argument, the records are sorted by default in ascending order.</span></span> 
  

