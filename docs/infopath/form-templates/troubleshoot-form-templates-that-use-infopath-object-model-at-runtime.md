---
title: Solucionar problemas de modelos de formulário que usam o modelo de objeto do InfoPath em tempo de executar
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
keywords:
- solução de problemas de modelos de formulário [infopath 2007], tempo de executar, modelos de formulário compatíveis com o InfoPath 2003, solução de problemas em tempo de executar
localization_priority: Normal
ms.assetid: 65e7882e-6397-4375-9bb4-d993d700d749
description: As seções a seguir descrevem cenários comuns de solução de problemas que você pode encontrar ao trabalhar com modelos de formulário de código gerenciado do InfoPath que usam o modelo de objeto compatível com o InfoPath 2003 fornecido pelo namespace Microsoft.Office.Interop.InfoPath.SemiTrust em tempo de executar.
ms.openlocfilehash: c7b4b65cc722e72ef155529a0b2aa66c4f6cfcff
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33414442"
---
# <a name="troubleshoot-form-templates-that-use-the-infopath-object-model-at-run-time"></a>Solucionar problemas de modelos de formulário que usam o modelo de objeto do InfoPath em tempo de executar

As seções a seguir descrevem cenários comuns de solução de problemas que você pode encontrar ao trabalhar com modelos de formulário de código gerenciado do InfoPath que usam o modelo de objeto compatível com o InfoPath 2003 fornecido pelo namespace **Microsoft.Office.Interop.InfoPath.SemiTrust** em tempo de executar. 
  
## <a name="display-notifications-for-unhandled-managed-code-exceptions-at-run-time"></a>Exibir notificações para exceções de código gerenciado não gerenciado em tempo de executar

Se você não usar o tratamento de exceção try-catch no código do formulário, o InfoPath exibirá informações sobre exceções não manipuladas na caixa de diálogo de erro do InfoPath durante a depuração e visualização. No entanto, por padrão, exceções sem tratamento não são exibidas na caixa de diálogo de erro do InfoPath em tempo de executar quando você implanta seu modelo de formulário de código gerenciado. Se você quiser exceções de código gerenciado exibidas em tempo de executar, siga o procedimento na seção "Manipulando exceções de código gerenciado" de Manipular erros usando o modelo de objeto do [InfoPath 2003.](how-to-handle-errors-using-the-infopath-2003-object-model.md)
  
## <a name="problems-with-managed-code-form-templates-after-deployment"></a>Problemas com modelos de formulário de código gerenciado após a implantação

Certifique-se de testar seu modelo de formulário de código gerenciado no local onde ele será finalmente implantado. Para obter informações sobre procedimentos de implantação, [consulte Implantar modelos de formulário do InfoPath com código.](how-to-deploy-infopath-form-templates-with-code.md) Para obter informações sobre cenários de segurança que afetam a implantação, consulte Sobre o [modelo de segurança para modelos de formulário com código.](about-the-security-model-for-form-templates-with-code.md)
  
Se você usar o utilitário de configuração do .NET Framework 1.1 e o grupo de códigos de Modelos de Formulário do InfoPath para adicionar permissões específicas para um modelo de formulário de código gerenciado, certifique-se de que a mesma política de segurança seja implantada em todos os computadores cliente. Além disso, se você estiver especificando **URLEvidence** que se refere a um local no computador local, certifique-se de que o local especificado refere-se à pasta onde a solução será finalmente implantada (não o mesmo local usado durante o desenvolvimento). Para obter informações sobre como definir as configurações de segurança do .NET Framework para um modelo de formulário de [](how-to-configure-security-settings-for-form-templates-with-code.md) código gerenciado, consulte a seção "Atribuindo FullTrust a Formulários em uma URL específica ou UNC" do tópico Definir configurações de segurança para modelos de formulário com código. 
  
## <a name="see-also"></a>Confira também

- [Sobre o modelo de segurança para modelos de formulário com código](about-the-security-model-for-form-templates-with-code.md)
- [Implantar modelos de formulário do InfoPath com código](how-to-deploy-infopath-form-templates-with-code.md)
- [Tratar erros usando o modelo de objeto do InfoPath 2003](how-to-handle-errors-using-the-infopath-2003-object-model.md)
- [Depurar projetos do InfoPath usando o modelo de objeto do InfoPath 2003](how-to-debug-infopath-projects-using-the-infopath-2003-object-model.md)

