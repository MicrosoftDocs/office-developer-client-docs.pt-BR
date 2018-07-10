---
title: Ação de Macro OpenPopup (aplicativo da web personalizado do Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 850de802-e417-4884-8d14-571de52aa391
description: Abre o modo de exibição especificado em uma janela pop-up.
ms.openlocfilehash: 01e0086dc0b54837cf5f095ec6ac5701b5b0b219
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19765198"
---
# <a name="openpopup-macro-action-access-custom-web-app"></a><span data-ttu-id="a8866-103">Ação de Macro OpenPopup (aplicativo da web personalizado do Access)</span><span class="sxs-lookup"><span data-stu-id="a8866-103">OpenPopup Macro Action (Access custom web app)</span></span>

<span data-ttu-id="a8866-104">Abre o modo de exibição especificado em uma janela pop-up.</span><span class="sxs-lookup"><span data-stu-id="a8866-104">Opens the specified view in a popup window.</span></span>
  
> [!IMPORTANT]
> <span data-ttu-id="a8866-p101">A Microsoft não recomenda mais criar e usar aplicativos Web do Access no SharePoint. Como alternativa, use o [Microsoft PowerApps](https://powerapps.microsoft.com/pt-br/) para criar soluções de negócios sem código para a Web e dispositivos móveis.</span><span class="sxs-lookup"><span data-stu-id="a8866-p101">Microsoft no longer recommends creating and using Access web apps in SharePoint. As an alternative, consider using [Microsoft PowerApps](https://powerapps.microsoft.com/pt-br/) to build no-code business solutions for the web and mobile devices.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="a8866-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="a8866-107">Syntax</span></span>

 <span data-ttu-id="a8866-108">**OpenPopup** (*Modo de exibição*, *onde =*, *Ordenar por*)</span><span class="sxs-lookup"><span data-stu-id="a8866-108">**OpenPopup** (*View*, *Where=*, *Order By*)</span></span> 
  
<span data-ttu-id="a8866-109">A ação **OpenPopup** contém os seguintes argumentos.</span><span class="sxs-lookup"><span data-stu-id="a8866-109">The **OpenPopup** action contains the following arguments.</span></span> 
  
|<span data-ttu-id="a8866-110">**Nome do argumento**</span><span class="sxs-lookup"><span data-stu-id="a8866-110">**Argument name**</span></span>|<span data-ttu-id="a8866-111">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="a8866-111">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="a8866-112">*View*</span><span class="sxs-lookup"><span data-stu-id="a8866-112">*View*</span></span>  <br/> |<span data-ttu-id="a8866-113">O nome da exibição a ser aberto.</span><span class="sxs-lookup"><span data-stu-id="a8866-113">The name of the view to open.</span></span>  <br/> |
| <span data-ttu-id="a8866-114">*Onde =*</span><span class="sxs-lookup"><span data-stu-id="a8866-114">*Where=*</span></span>  <br/> |<span data-ttu-id="a8866-115">Uma cláusula SQL WHERE válida (sem a palavra onde) que restringe os registros no modo de exibição.</span><span class="sxs-lookup"><span data-stu-id="a8866-115">A valid SQL WHERE clause (without the word WHERE) that restricts the records in the view.</span></span>  <br/> |
| <span data-ttu-id="a8866-116">*Classificado por*</span><span class="sxs-lookup"><span data-stu-id="a8866-116">*Order By*</span></span>  <br/> |<span data-ttu-id="a8866-117">Uma expressão de cadeia de caracteres que inclui o nome do(s) campo(s) no(s) qual(is) serão classificados os registros e as palavras-chave CRESC ou DECRESC opcionais.</span><span class="sxs-lookup"><span data-stu-id="a8866-117">A string expression that includes the name of the field or fields on which to sort records and the optional ASC or DESC keywords.</span></span> <span data-ttu-id="a8866-118">Por padrão, esse argumento estiver em branco.</span><span class="sxs-lookup"><span data-stu-id="a8866-118">By default, this argument is blank.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a8866-119">Coment�rios</span><span class="sxs-lookup"><span data-stu-id="a8866-119">Remarks</span></span>

<span data-ttu-id="a8866-120">A macro atual termina depois que a ação **OpenPopup** é processada.</span><span class="sxs-lookup"><span data-stu-id="a8866-120">The current macro ends once the **OpenPopup** action is processed.</span></span> 
  
<span data-ttu-id="a8866-121">Qualquer classificação ou filtragem aplicada pelo usuário é limpa quando a ação **OpenPopup** é chamada.</span><span class="sxs-lookup"><span data-stu-id="a8866-121">Any sorting or filtering applied by the user is cleared when the **OpenPopup** action is called.</span></span> 
  
<span data-ttu-id="a8866-122">O argumento *OrderBy* é o nome do campo ou dos campos nos quais você deseja classificar os registros.</span><span class="sxs-lookup"><span data-stu-id="a8866-122">The  *OrderBy*  argument is the name of the field or fields on which you want to sort records.</span></span> <span data-ttu-id="a8866-123">Quando você usa mais de um nome de campo, separe-os com vírgula (,).</span><span class="sxs-lookup"><span data-stu-id="a8866-123">When you use more than one field name, separate the names with a comma (,).</span></span> 
  
<span data-ttu-id="a8866-124">Quando você define o argumento *OrderBy* , os registros são classificados por padrão em ordem crescente.</span><span class="sxs-lookup"><span data-stu-id="a8866-124">When you set the  *OrderBy*  argument, the records are sorted by default in ascending order.</span></span> 
  

