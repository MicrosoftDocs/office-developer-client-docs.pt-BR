---
title: Visualizar e depurar modelos de formulário que exigem confiança total
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
keywords:
- depuração [infopath 2007], modelos de formulário compatíveis com o InfoPath 2003, visualização de modelos de formulário compatíveis com o InfoPath 2003, modelos de formulário [InfoPath 2007], visualização de modelos de formulário compatíveis com 2003 [InfoPath 2007], depuração compatível com 2003, depuração de modelos de formulário compatíveis com o InfoPath 2003
localization_priority: Normal
ms.assetid: 5c491666-06f0-42ec-967e-1c70cd5e03a0
description: Por padrão, se você tentar depurar ou visualizar um projeto de código gerenciado que contenha código que invoque um membro do modelo de objeto que exija confiança total, como a propriedade LoginName, que exige acesso a informações sobre o domínio de logon do usuário, o Microsoft InfoPath exibirá as seguintes mensagens de erro.
ms.openlocfilehash: 0780db286e2ca9cef381c2d24cb621c7c243dcb7
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33411257"
---
# <a name="preview-and-debug-form-templates-that-require-full-trust"></a><span data-ttu-id="ed010-104">Visualizar e depurar modelos de formulário que exigem confiança total</span><span class="sxs-lookup"><span data-stu-id="ed010-104">Preview and Debug Form Templates that Require Full Trust</span></span>

<span data-ttu-id="ed010-105">Por padrão, se você tentar depurar ou visualizar um projeto de código gerenciado que contenha código que invoque um membro do modelo de objeto que exija confiança total, como a propriedade **LoginName,** que exige acesso a informações sobre o domínio de logon do usuário, o Microsoft InfoPath exibirá as seguintes mensagens de erro.</span><span class="sxs-lookup"><span data-stu-id="ed010-105">By default, if you attempt to debug or preview a managed-code project that contains code that invokes an object model member that requires full trust, such as the **LoginName** property which requires access to information about the user's login domain, Microsoft InfoPath will display the following error messages.</span></span> 
  
<span data-ttu-id="ed010-106">Durante a visualização:</span><span class="sxs-lookup"><span data-stu-id="ed010-106">When previewing:</span></span>
  
<span data-ttu-id="ed010-107">"Ocorreu uma exceção sem forma no código do formulário."</span><span class="sxs-lookup"><span data-stu-id="ed010-107">"An unhandled exception has occurred in the form's code."</span></span> <span data-ttu-id="ed010-108">Seguido por " InfoPath não pode concluir esta ação, devido a um erro no código do formulário."</span><span class="sxs-lookup"><span data-stu-id="ed010-108">Followed by, "InfoPath cannot complete this action, because of an error in the form's code."</span></span>
  
<span data-ttu-id="ed010-109">Durante a depuração:</span><span class="sxs-lookup"><span data-stu-id="ed010-109">When debugging:</span></span>
  
<span data-ttu-id="ed010-110">O foco se moverá para a linha de código no editor de código que está chamando o membro que exige confiança total, e a seguinte mensagem será exibida: " **SecurityException** não foi asseada pelo código de usuário - Falha na solicitação".</span><span class="sxs-lookup"><span data-stu-id="ed010-110">Focus will move to the line of code in the code editor that is calling the member that requires full trust, and the following message will be displayed: " **SecurityException** was unhandled by user code - Request failed".</span></span> 
  
<span data-ttu-id="ed010-111">Para permitir que a lógica de negócios do modelo de formulário chame esse membro quando ele estiver sendo  depurado ou visualizado, você deve definir o nível de segurança do modelo de formulário como Confiança Total, conforme descrito no procedimento a seguir.</span><span class="sxs-lookup"><span data-stu-id="ed010-111">To allow the form template's business logic to call this member when it is being debugged or previewed, you must set your form template's security level to **Full Trust** as described in the following procedure.</span></span> 
  
## <a name="configuring-a-managed-code-form-template-that-requires-full-trust"></a><span data-ttu-id="ed010-112">Configurando um modelo de formulário de código gerenciado que requer confiança total</span><span class="sxs-lookup"><span data-stu-id="ed010-112">Configuring a Managed Code Form Template that Requires Full Trust</span></span>

### <a name="set-your-forms-security-level-to-full-trust"></a><span data-ttu-id="ed010-113">Definir o nível de segurança do formulário como Confiança Total</span><span class="sxs-lookup"><span data-stu-id="ed010-113">Set your form's security level to Full Trust</span></span>

1. <span data-ttu-id="ed010-114">No InfoPath, abra o modelo de formulário no modo de design.</span><span class="sxs-lookup"><span data-stu-id="ed010-114">In InfoPath, open the form template in design mode.</span></span>
    
2. <span data-ttu-id="ed010-115">Clique na guia **Arquivo** e em **Opções de Formulário**. Depois, clique na guia **Informações**.</span><span class="sxs-lookup"><span data-stu-id="ed010-115">Click the **File** tab, and then click **Form Options** on the **Info** tab.</span></span> 
    
3. <span data-ttu-id="ed010-116">Na lista **Categoria,** clique em **Segurança e Confiança.**</span><span class="sxs-lookup"><span data-stu-id="ed010-116">In the **Category** list, click **Security and Trust.**</span></span>
    
4. <span data-ttu-id="ed010-117">Em **Nível de Segurança,** desempate **Determinar automaticamente o nível de segurança.**</span><span class="sxs-lookup"><span data-stu-id="ed010-117">Under **Security Level**, clear **Automatically determine security level**.</span></span>
    
5. <span data-ttu-id="ed010-118">Selecione **Confiança Total** e clique em **OK.**</span><span class="sxs-lookup"><span data-stu-id="ed010-118">Select **Full Trust**, and then click **OK**.</span></span>
    
<span data-ttu-id="ed010-119">Depois que esse procedimento for executado, você poderá depurar seu projeto conforme descrito em Visualizar e Depurar modelos de formulário do [InfoPath com código.](how-to-preview-and-debug-infopath-form-templates-with-code.md)</span><span class="sxs-lookup"><span data-stu-id="ed010-119">After this procedure is performed, you can debug your project as described in [Preview and Debug InfoPath Form Templates with Code](how-to-preview-and-debug-infopath-form-templates-with-code.md).</span></span>
  
> [!NOTE]
> <span data-ttu-id="ed010-120">A implantação bem-sucedida de um modelo de formulário de código gerenciado que exige confiança total requer etapas adicionais, como assinar digitalmente ou instalar e registrar o modelo de formulário.</span><span class="sxs-lookup"><span data-stu-id="ed010-120">Successfully deploying a managed code form template that requires full trust requires additional steps, such as digitally signing, or installing and registering the form template.</span></span> <span data-ttu-id="ed010-121">Para obter informações sobre como implantar um modelo de formulário de código gerenciado depois que ele for depurado, consulte Implantar modelos de formulário do [InfoPath com código.](how-to-deploy-infopath-form-templates-with-code.md)</span><span class="sxs-lookup"><span data-stu-id="ed010-121">For information on deploying a managed code form template after it is debugged see, [Deploy InfoPath Form Templates with Code](how-to-deploy-infopath-form-templates-with-code.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="ed010-122">Confira também</span><span class="sxs-lookup"><span data-stu-id="ed010-122">See also</span></span>



[<span data-ttu-id="ed010-123">Visualizar e depurar modelos de formulário do InfoPath com código</span><span class="sxs-lookup"><span data-stu-id="ed010-123">Preview and Debug InfoPath Form Templates with Code</span></span>](how-to-preview-and-debug-infopath-form-templates-with-code.md)
  
[<span data-ttu-id="ed010-124">Implantar modelos de formulário do InfoPath com código</span><span class="sxs-lookup"><span data-stu-id="ed010-124">Deploy InfoPath Form Templates with Code</span></span>](how-to-deploy-infopath-form-templates-with-code.md)

