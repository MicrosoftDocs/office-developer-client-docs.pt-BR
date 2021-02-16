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
# <a name="preview-and-debug-form-templates-that-require-full-trust"></a>Visualizar e depurar modelos de formulário que exigem confiança total

Por padrão, se você tentar depurar ou visualizar um projeto de código gerenciado que contenha código que invoque um membro do modelo de objeto que exija confiança total, como a propriedade **LoginName,** que exige acesso a informações sobre o domínio de logon do usuário, o Microsoft InfoPath exibirá as seguintes mensagens de erro. 
  
Durante a visualização:
  
"Ocorreu uma exceção sem forma no código do formulário." Seguido por " InfoPath não pode concluir esta ação, devido a um erro no código do formulário."
  
Durante a depuração:
  
O foco se moverá para a linha de código no editor de código que está chamando o membro que exige confiança total, e a seguinte mensagem será exibida: " **SecurityException** não foi asseada pelo código de usuário - Falha na solicitação". 
  
Para permitir que a lógica de negócios do modelo de formulário chame esse membro quando ele estiver sendo  depurado ou visualizado, você deve definir o nível de segurança do modelo de formulário como Confiança Total, conforme descrito no procedimento a seguir. 
  
## <a name="configuring-a-managed-code-form-template-that-requires-full-trust"></a>Configurando um modelo de formulário de código gerenciado que requer confiança total

### <a name="set-your-forms-security-level-to-full-trust"></a>Definir o nível de segurança do formulário como Confiança Total

1. No InfoPath, abra o modelo de formulário no modo de design.
    
2. Clique na guia **Arquivo** e em **Opções de Formulário**. Depois, clique na guia **Informações**. 
    
3. Na lista **Categoria,** clique em **Segurança e Confiança.**
    
4. Em **Nível de Segurança,** desempate **Determinar automaticamente o nível de segurança.**
    
5. Selecione **Confiança Total** e clique em **OK.**
    
Depois que esse procedimento for executado, você poderá depurar seu projeto conforme descrito em Visualizar e Depurar modelos de formulário do [InfoPath com código.](how-to-preview-and-debug-infopath-form-templates-with-code.md)
  
> [!NOTE]
> A implantação bem-sucedida de um modelo de formulário de código gerenciado que exige confiança total requer etapas adicionais, como assinar digitalmente ou instalar e registrar o modelo de formulário. Para obter informações sobre como implantar um modelo de formulário de código gerenciado depois que ele for depurado, consulte Implantar modelos de formulário do [InfoPath com código.](how-to-deploy-infopath-form-templates-with-code.md) 
  
## <a name="see-also"></a>Confira também



[Visualizar e depurar modelos de formulário do InfoPath com código](how-to-preview-and-debug-infopath-form-templates-with-code.md)
  
[Implantar modelos de formulário do InfoPath com código](how-to-deploy-infopath-form-templates-with-code.md)

