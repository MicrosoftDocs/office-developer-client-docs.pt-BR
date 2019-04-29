---
title: Solucionar problemas de modelos de formulário que usam o modelo de objeto do InfoPath em tempo de execução
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
keywords:
- Solucionando problemas de modelos de formulário [InfoPath 2007], tempo de execução, modelos de formulário compatíveis com o InfoPath 2003, solução de problemas em tempo de execução
localization_priority: Normal
ms.assetid: 65e7882e-6397-4375-9bb4-d993d700d749
description: As seções a seguir descrevem cenários de solução de problemas comuns que você pode encontrar ao trabalhar com modelos de formulário de código gerenciado do InfoPath que usam o modelo de objeto compatível com o InfoPath 2003 fornecido pelo Microsoft. Office. Interop. InfoPath. SemiTrust namespace em tempo de execução.
ms.openlocfilehash: c7b4b65cc722e72ef155529a0b2aa66c4f6cfcff
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33414442"
---
# <a name="troubleshoot-form-templates-that-use-the-infopath-object-model-at-run-time"></a>Solucionar problemas de modelos de formulário que usam o modelo de objeto do InfoPath em tempo de execução

As seções a seguir descrevem cenários de solução de problemas comuns que você pode encontrar ao trabalhar com modelos de formulário de código gerenciado do InfoPath que usam o modelo de objeto compatível com o InfoPath 2003 fornecido pelo ** Namespace Microsoft. Office. Interop. InfoPath. SemiTrust** no tempo de execução. 
  
## <a name="display-notifications-for-unhandled-managed-code-exceptions-at-run-time"></a>Exibir notificações para exceções de código gerenciado não manipuladas no tempo de execução

Se você não usar a manipulação de exceção de tentativa-catch no seu código de formulário, o InfoPath exibirá informações sobre exceções não tratadas na caixa de diálogo de erro do InfoPath durante a depuração e a visualização. No enTanto, por padrão, as exceções não manipuladas não são exibidas na caixa de diálogo de erro do InfoPath em tempo de execução quando você implanta seu modelo de formulário de código gerenciado. Se você deseja que exceções de código gerenciado sejam exibidas no tempo de execução, siga o procedimento na seção "manipulando exceções de código gerenciados" de [tratar erros usando o modelo de objeto do InfoPath 2003](how-to-handle-errors-using-the-infopath-2003-object-model.md).
  
## <a name="problems-with-managed-code-form-templates-after-deployment"></a>Problemas com modelos de formulário de código gerenciado após a implantação

Certifique-se de testar o modelo de formulário de código gerenciado no local onde ele será implantado. Para obter informações sobre procedimentos de implantação, consulte [implantar modelos de formulário do InfoPath com código](how-to-deploy-infopath-form-templates-with-code.md). Para obter informações sobre cenários de segurança que afetam a implantação, consulte [sobre o modelo de segurança para modelos de formulário com código](about-the-security-model-for-form-templates-with-code.md).
  
Se você usar o utilitário de configuração do .NET Framework 1,1 e o grupo de códigos de modelos de formulário do InfoPath para adicionar permissões específicas para um modelo de formulário de código gerenciado, certifique-se de que a mesma política de segurança está implantada em todos os computadores cliente. Além disso, se você estiver especificando **URLEvidence** que se referem a um local no computador local, certifique-se de que o local especificado se refere à pasta em que a solução será finalmente implantada (não o mesmo local usado durante o desenvolvimento). Para obter informações sobre como definir as configurações de segurança do .NET Framework para um modelo de formulário de código gerenciado, consulte a seção "atribuindo FullTrust a formulários em uma URL específica ou UNC" do tópico [definir configurações de segurança para modelos de formulário com código](how-to-configure-security-settings-for-form-templates-with-code.md) . 
  
## <a name="see-also"></a>Confira também

- [Sobre o modelo de segurança para modelos de formulário com código](about-the-security-model-for-form-templates-with-code.md)
- [Implantar modelos de formulário do InfoPath com código](how-to-deploy-infopath-form-templates-with-code.md)
- [Manipular erros usando o modelo de objeto do InfoPath 2003](how-to-handle-errors-using-the-infopath-2003-object-model.md)
- [Depurar projetos do InfoPath usando o modelo de objeto do InfoPath 2003](how-to-debug-infopath-projects-using-the-infopath-2003-object-model.md)

