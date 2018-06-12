---
title: Solucionar problemas de modelos de formulário que usam o modelo de objeto do InfoPath em tempo de execução
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
keywords:
- tempo de modelos [infopath 2007], executados formulário de solução de problemas, modelos de formulário compatíveis com o InfoPath 2003, solução de problemas em tempo de execução
localization_priority: Normal
ms.assetid: 65e7882e-6397-4375-9bb4-d993d700d749
description: As próximas seções descrevem os cenários de solução de problemas comuns que você pode encontrar ao trabalhar com modelos de formulário de código gerenciado do InfoPath que usam o modelo de objeto compatível com o InfoPath 2003 fornecido pelo SemiTrust namespace em tempo de execução.
ms.openlocfilehash: 8c83679a0cd61fae212b3143b6b0131da92ac7f9
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19765714"
---
# <a name="troubleshoot-form-templates-that-use-the-infopath-object-model-at-run-time"></a>Solucionar problemas de modelos de formulário que usam o modelo de objeto do InfoPath em tempo de execução

As próximas seções descrevem os cenários de solução de problemas comuns que você pode encontrar ao trabalhar com modelos de formulário de código gerenciado do InfoPath que usam o modelo de objeto compatível com o InfoPath 2003 fornecido pelo ** SemiTrust** namespace em tempo de execução. 
  
## <a name="display-notifications-for-unhandled-managed-code-exceptions-at-run-time"></a>Exibir notificações para exceções não tratadas de código gerenciado em tempo de execução

Se você não usar try-catch de tratamento de exceção no seu código de formulário, o InfoPath exibirá informações sobre exceções não tratadas na caixa de diálogo de erro do InfoPath durante a depuração e visualização. No entanto, por padrão, exceções não tratadas não são exibidas na caixa de diálogo de erro do InfoPath em tempo de execução quando você implanta o seu modelo de formulário de código gerenciado. Se você quiser exibidas em tempo de execução de exceções de código gerenciado, siga o procedimento na seção "Tratando a exceções de código gerenciado" de [Lidar com erros usando o modelo de objeto do InfoPath 2003](how-to-handle-errors-using-the-infopath-2003-object-model.md).
  
## <a name="problems-with-managed-code-form-templates-after-deployment"></a>Problemas com os modelos de formulário de código gerenciado após a implantação

Certifique-se de testar seu modelo de formulário de código gerenciado no local onde ele será finalmente implantado. Para obter informações sobre procedimentos de implantação, consulte [Implantar modelos de formulário do InfoPath com código](how-to-deploy-infopath-form-templates-with-code.md). Para obter informações sobre cenários de segurança que afetam a implantação, consulte [Sobre o modelo de segurança para modelos de formulário com código](about-the-security-model-for-form-templates-with-code.md).
  
Se você usar o utilitário de configuração do .NET Framework 1.1 e o grupo de códigos de modelos de formulário do InfoPath para adicionar permissões específicas de um modelo de formulário de código gerenciado, certifique-se de que a mesma política de segurança é implantada em todos os computadores cliente. Além disso, se você está especificando **URLEvidence** que se refere a um local no computador local, certifique-se de finalmente local especificado refere-se para a pasta onde a solução será implantada (não o mesmo local usado durante o desenvolvimento). Para obter informações sobre como configurar as configurações de segurança do .NET Framework para um modelo de formulário de código gerenciado, consulte a seção "Atribuindo FullTrust para formulários em um específicos URL ou UNC" do tópico [Configurar definições de segurança para modelos de formulário com código](how-to-configure-security-settings-for-form-templates-with-code.md) . 
  
## <a name="see-also"></a>Confira também

- [Sobre o modelo de segurança para modelos de formulário com código](about-the-security-model-for-form-templates-with-code.md)
- [Implantar modelos de formulário do InfoPath com código](how-to-deploy-infopath-form-templates-with-code.md)
- [Manipular erros usando o modelo de objeto do InfoPath 2003](how-to-handle-errors-using-the-infopath-2003-object-model.md)
- [Depurar projetos do InfoPath usando o modelo de objeto do InfoPath 2003](how-to-debug-infopath-projects-using-the-infopath-2003-object-model.md)

