---
title: Bloco de Dados EditarRegiscord (aplicativo Web personalizado do Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
localization_priority: Normal
ms.assetid: 54975434-78b2-4010-b2f9-f277831fa92e
description: Você pode usar o bloco de dados EditarRegistro para alterar os valores contidos em um registro existente.
ms.openlocfilehash: 0d9ef6c7689b44a0304309a7537e744eff97c809
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418341"
---
# <a name="editrecord-data-block-access-custom-web-app"></a><span data-ttu-id="b83bb-103">Bloco de Dados EditarRegiscord (aplicativo Web personalizado do Access)</span><span class="sxs-lookup"><span data-stu-id="b83bb-103">EditRecord Data Block (Access custom web app)</span></span>

<span data-ttu-id="b83bb-104">Você pode usar o bloco de dados **EditarRegistro** para alterar os valores contidos em um registro existente.</span><span class="sxs-lookup"><span data-stu-id="b83bb-104">You can use the **EditRecord** data block to change the values contained in an existing record.</span></span> 
  
> [!IMPORTANT]
> <span data-ttu-id="b83bb-p101">A Microsoft não recomenda mais criar e usar aplicativos Web do Access no SharePoint. Como alternativa, use o [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) para criar soluções de negócios sem código para a Web e dispositivos móveis.</span><span class="sxs-lookup"><span data-stu-id="b83bb-p101">Microsoft no longer recommends creating and using Access web apps in SharePoint. As an alternative, consider using [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) to build no-code business solutions for the web and mobile devices.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="b83bb-107">O bloco de dados **EditarRegistro** está disponível somente em Macros de Dados.</span><span class="sxs-lookup"><span data-stu-id="b83bb-107">The **EditRecord** data block is available only in Data Macros.</span></span> 
  
## <a name="setting"></a><span data-ttu-id="b83bb-108">Setting</span><span class="sxs-lookup"><span data-stu-id="b83bb-108">Setting</span></span>

<span data-ttu-id="b83bb-109">O bloco de dados **EditarRegistro** tem os seguintes argumentos.</span><span class="sxs-lookup"><span data-stu-id="b83bb-109">The **EditRecord** data block has the following arguments.</span></span> 
  
|<span data-ttu-id="b83bb-110">**Argumento**</span><span class="sxs-lookup"><span data-stu-id="b83bb-110">**Argument**</span></span>|<span data-ttu-id="b83bb-111">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="b83bb-111">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="b83bb-112">**Alias**</span><span class="sxs-lookup"><span data-stu-id="b83bb-112">**Alias**</span></span> <br/> |<span data-ttu-id="b83bb-113">Uma cadeia de caracteres que identifica o registro a ser editado.</span><span class="sxs-lookup"><span data-stu-id="b83bb-113">A string that identifies the record to edit.</span></span> <span data-ttu-id="b83bb-114">Se o  *argumento Alias*  não for especificado, o registro atual será editado.</span><span class="sxs-lookup"><span data-stu-id="b83bb-114">If the  *Alias*  argument is not specified, then the current record is edited.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="b83bb-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="b83bb-115">Remarks</span></span>

<span data-ttu-id="b83bb-116">Após a **instrução EditRecord,** você pode inserir um bloco de comandos que será executado antes que as alterações no registro sejam comprometidas.</span><span class="sxs-lookup"><span data-stu-id="b83bb-116">After the **EditRecord** statement, you can insert a block of commands that will execute before the changes to the record are committed.</span></span> <span data-ttu-id="b83bb-117">As ações a seguir estão disponíveis em um **bloco de dados EditarRegiso.**</span><span class="sxs-lookup"><span data-stu-id="b83bb-117">The following actions are available in an **EditRecord** data block.</span></span> 
  
||
|:-----|
|[<span data-ttu-id="b83bb-118">Ação de macro CancelRecordChange</span><span class="sxs-lookup"><span data-stu-id="b83bb-118">CancelRecordChange Macro Action</span></span>](cancelrecordchange-macro-action-access-custom-web-app.md) <br/> |
|[<span data-ttu-id="b83bb-119">Instrução de macro de comentário</span><span class="sxs-lookup"><span data-stu-id="b83bb-119">Comment Macro Statement</span></span>](comment-macro-block-access-custom-web-app.md) <br/> |
|[<span data-ttu-id="b83bb-120">Instrução de macro de grupo</span><span class="sxs-lookup"><span data-stu-id="b83bb-120">Group Macro Statement</span></span>](group-macro-block-access-custom-web-app.md) <br/> |
|[<span data-ttu-id="b83bb-121">Instrução de macro Se...Então...Senão</span><span class="sxs-lookup"><span data-stu-id="b83bb-121">If...Then...Else Macro Statement</span></span>](ifthenelse-macro-block-access-custom-web-app.md) <br/> |
|[<span data-ttu-id="b83bb-122">Ação de macro SetField</span><span class="sxs-lookup"><span data-stu-id="b83bb-122">SetField Macro Action</span></span>](setfield-macro-action-access-custom-web-app.md) <br/> |
|[<span data-ttu-id="b83bb-123">Ação de macro SetLocalVar</span><span class="sxs-lookup"><span data-stu-id="b83bb-123">SetLocalVar Macro Action</span></span>](setlocalvar-macro-action-access-custom-web-app.md) <br/> |
   
<span data-ttu-id="b83bb-124">Use a ação **DefinirCampo** para especificar os novos valores de um campo no registro editado.</span><span class="sxs-lookup"><span data-stu-id="b83bb-124">Use the **SetField** action to specify the new values of a field in the edited record.</span></span> 
  
<span data-ttu-id="b83bb-125">Você pode usar um **If... Então... Instrução Else** para executar operações com base em uma condição.</span><span class="sxs-lookup"><span data-stu-id="b83bb-125">You can use an **If...Then...Else** statement to perform operations based on a condition.</span></span> 
  
<span data-ttu-id="b83bb-p104">Para cancelar a edição de um registro, use a ação **CancelarAlteraçãodeRegistro**. Dessa forma, as alterações não são atribuídas e o bloco de dados **EditarRegistro** é encerrado.</span><span class="sxs-lookup"><span data-stu-id="b83bb-p104">To cancel the editing of a record, use the **CancelRecordChange** action. This prevents the changes from being committed and exits the **EditRecord** data block.</span></span> 
  
<span data-ttu-id="b83bb-128">Você pode usar a variável local **IdentidadedeRegistroCriadapelaÚltimaVez** para executá-la com o último registro criado em um bloco de dados **CriarRegistro**.</span><span class="sxs-lookup"><span data-stu-id="b83bb-128">You can use the **LastCreateRecordIdentity** local variable to work with last record created in a **CreateRecord** data block.</span></span> <span data-ttu-id="b83bb-129">Por exemplo, use a sintaxe a seguir para se referir ao campo AtribuídoA do registro criado mais recentemente:</span><span class="sxs-lookup"><span data-stu-id="b83bb-129">For example, use the following syntax to refer to the AssignedTo field of the most recently created record:</span></span> 
  
`[LastCreateRecordIdentity].[AssignedTo]`


