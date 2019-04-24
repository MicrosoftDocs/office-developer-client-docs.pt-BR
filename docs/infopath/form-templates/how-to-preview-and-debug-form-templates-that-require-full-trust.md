---
title: Visualizar e depurar modelos de formulário que exigem confiança total
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
keywords:
- Debugging [InfoPath 2007], modelos de formulário compatíveis com o InfoPath 2003, visualizando modelos de formulário compatíveis com o InfoPath 2003, modelos de formulário [InfoPath 2007], visualizações 2003 compatíveis, modelos de formulário [InfoPath 2007], depuração compatível com o 2003 Modelos de formulário compatíveis com o InfoPath 2003
localization_priority: Normal
ms.assetid: 5c491666-06f0-42ec-967e-1c70cd5e03a0
description: Por padrão, se você tentar depurar ou Visualizar um projeto de código gerenciado que contenha código que invoque um membro de modelo de objeto que requer confiança total, como a Propriedade LoginName que requer acesso a informações sobre o domínio de logon do usuário, a Microsoft O InfoPath exibirá as seguintes mensagens de erro.
ms.openlocfilehash: 0780db286e2ca9cef381c2d24cb621c7c243dcb7
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32303595"
---
# <a name="preview-and-debug-form-templates-that-require-full-trust"></a><span data-ttu-id="dc9ec-104">Visualizar e depurar modelos de formulário que exigem confiança total</span><span class="sxs-lookup"><span data-stu-id="dc9ec-104">Preview and Debug Form Templates that Require Full Trust</span></span>

<span data-ttu-id="dc9ec-105">Por padrão, se você tentar depurar ou Visualizar um projeto de código gerenciado que contenha código que invoque um membro de modelo de objeto que requer confiança total, como a propriedade **LoginName** que requer acesso a informações sobre o domínio de logon do usuário, O Microsoft InfoPath exibirá as seguintes mensagens de erro.</span><span class="sxs-lookup"><span data-stu-id="dc9ec-105">By default, if you attempt to debug or preview a managed-code project that contains code that invokes an object model member that requires full trust, such as the **LoginName** property which requires access to information about the user's login domain, Microsoft InfoPath will display the following error messages.</span></span> 
  
<span data-ttu-id="dc9ec-106">Ao Visualizar:</span><span class="sxs-lookup"><span data-stu-id="dc9ec-106">When previewing:</span></span>
  
<span data-ttu-id="dc9ec-107">"Uma exceção sem tratamento ocorreu no código do formulário."</span><span class="sxs-lookup"><span data-stu-id="dc9ec-107">"An unhandled exception has occurred in the form's code."</span></span> <span data-ttu-id="dc9ec-108">Seguido de, "o InfoPath não pode concluir esta ação devido a um erro no código do formulário."</span><span class="sxs-lookup"><span data-stu-id="dc9ec-108">Followed by, "InfoPath cannot complete this action, because of an error in the form's code."</span></span>
  
<span data-ttu-id="dc9ec-109">Ao depurar:</span><span class="sxs-lookup"><span data-stu-id="dc9ec-109">When debugging:</span></span>
  
<span data-ttu-id="dc9ec-110">O foco se moverá para a linha de código no editor de código que está chamando o membro que requer confiança total, e a seguinte mensagem será exibida: \*\*\*\* "SecurityException não foi manipulado pelo código do usuário-falha na solicitação".</span><span class="sxs-lookup"><span data-stu-id="dc9ec-110">Focus will move to the line of code in the code editor that is calling the member that requires full trust, and the following message will be displayed: " **SecurityException** was unhandled by user code - Request failed".</span></span> 
  
<span data-ttu-id="dc9ec-111">Para permitir que a lógica de negócios do modelo de formulário Chame esse membro quando ele estiver sendo depurado ou visualizado, você deve definir o nível de segurança do modelo de formulário como **confiança total** , conforme descrito no procedimento a seguir.</span><span class="sxs-lookup"><span data-stu-id="dc9ec-111">To allow the form template's business logic to call this member when it is being debugged or previewed, you must set your form template's security level to **Full Trust** as described in the following procedure.</span></span> 
  
## <a name="configuring-a-managed-code-form-template-that-requires-full-trust"></a><span data-ttu-id="dc9ec-112">ConFigurando um modelo de formulário de código gerenciado que requer confiança total</span><span class="sxs-lookup"><span data-stu-id="dc9ec-112">Configuring a Managed Code Form Template that Requires Full Trust</span></span>

### <a name="set-your-forms-security-level-to-full-trust"></a><span data-ttu-id="dc9ec-113">Definir o nível de segurança do formulário como confiança total</span><span class="sxs-lookup"><span data-stu-id="dc9ec-113">Set your form's security level to Full Trust</span></span>

1. <span data-ttu-id="dc9ec-114">No InfoPath, abra o modelo de formulário no modo de design.</span><span class="sxs-lookup"><span data-stu-id="dc9ec-114">In InfoPath, open the form template in design mode.</span></span>
    
2. <span data-ttu-id="dc9ec-115">Clique na guia **Arquivo** e em **Opções de Formulário**. Depois, clique na guia **Informações**.</span><span class="sxs-lookup"><span data-stu-id="dc9ec-115">Click the **File** tab, and then click **Form Options** on the **Info** tab.</span></span> 
    
3. <span data-ttu-id="dc9ec-116">Na lista **categoria** , clique em **segurança e confiança.**</span><span class="sxs-lookup"><span data-stu-id="dc9ec-116">In the **Category** list, click **Security and Trust.**</span></span>
    
4. <span data-ttu-id="dc9ec-117">Em **nível de segurança**, desmarque **determinar automaticamente o nível de segurança**.</span><span class="sxs-lookup"><span data-stu-id="dc9ec-117">Under **Security Level**, clear **Automatically determine security level**.</span></span>
    
5. <span data-ttu-id="dc9ec-118">Selecione **confiança total**e clique em **OK**.</span><span class="sxs-lookup"><span data-stu-id="dc9ec-118">Select **Full Trust**, and then click **OK**.</span></span>
    
<span data-ttu-id="dc9ec-119">Depois que esse procedimento for executado, você poderá depurar seu projeto conforme descrito em [Visualizar e depurar modelos de formulário do InfoPath com código](how-to-preview-and-debug-infopath-form-templates-with-code.md).</span><span class="sxs-lookup"><span data-stu-id="dc9ec-119">After this procedure is performed, you can debug your project as described in [Preview and Debug InfoPath Form Templates with Code](how-to-preview-and-debug-infopath-form-templates-with-code.md).</span></span>
  
> [!NOTE]
> <span data-ttu-id="dc9ec-120">A implantação bem-sucedida de um modelo de formulário de código gerenciado que requer confiança total requer etapas adicionais, como assinatura digital ou instalação e registro do modelo de formulário.</span><span class="sxs-lookup"><span data-stu-id="dc9ec-120">Successfully deploying a managed code form template that requires full trust requires additional steps, such as digitally signing, or installing and registering the form template.</span></span> <span data-ttu-id="dc9ec-121">Para obter informações sobre a implantação de um modelo de formulário de código gerenciado depois de ser depurado, consulte [implantar modelos de formulário do InfoPath com código](how-to-deploy-infopath-form-templates-with-code.md).</span><span class="sxs-lookup"><span data-stu-id="dc9ec-121">For information on deploying a managed code form template after it is debugged see, [Deploy InfoPath Form Templates with Code](how-to-deploy-infopath-form-templates-with-code.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="dc9ec-122">Confira também</span><span class="sxs-lookup"><span data-stu-id="dc9ec-122">See also</span></span>



[<span data-ttu-id="dc9ec-123">Visualizar e depurar modelos de formulário do InfoPath com código</span><span class="sxs-lookup"><span data-stu-id="dc9ec-123">Preview and Debug InfoPath Form Templates with Code</span></span>](how-to-preview-and-debug-infopath-form-templates-with-code.md)
  
[<span data-ttu-id="dc9ec-124">Implantar modelos de formulário do InfoPath com código</span><span class="sxs-lookup"><span data-stu-id="dc9ec-124">Deploy InfoPath Form Templates with Code</span></span>](how-to-deploy-infopath-form-templates-with-code.md)

