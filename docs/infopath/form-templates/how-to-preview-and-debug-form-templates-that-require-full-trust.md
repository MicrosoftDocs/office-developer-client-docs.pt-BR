---
title: Visualizar e depurar modelos de formulário que exigem confiança total
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
keywords:
- depuração de modelos de formulário do [infopath 2007], infopath 2003 compatíveis, visualização de modelos de formulário compatíveis com o InfoPath 2003, modelos de formulário [InfoPath 2007], visualização 2003 compatíveis, 2003 compatíveis, depuração de depuração de modelos de formulário [InfoPath 2007] Modelos de formulário compatíveis com o InfoPath 2003
localization_priority: Normal
ms.assetid: 5c491666-06f0-42ec-967e-1c70cd5e03a0
description: Por padrão, se você tentar depurar ou projeto de visualização de um código gerenciado que contém o código que invoca um membro de modelo de objeto que requer confiança total, tais como a propriedade LoginName que exige acesso a informações sobre o domínio de logon do usuário, Microsoft InfoPath exibirá as seguintes mensagens de erro.
ms.openlocfilehash: e9077b4ec0f8369b869e986020e4860f325fc023
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19765602"
---
# <a name="preview-and-debug-form-templates-that-require-full-trust"></a>Visualizar e depurar modelos de formulário que exigem confiança total

Por padrão, se você tentar depurar ou projeto de visualização de um código gerenciado que contém o código que invoca um membro de modelo de objeto que requer confiança total, tais como a propriedade **LoginName** que exige acesso a informações sobre o domínio de logon do usuário, Microsoft InfoPath exibirá as seguintes mensagens de erro. 
  
Ao pré-visualizar:
  
"Uma exceção não tratada ocorreu no código do formulário." Seguido, "InfoPath não é possível concluir esta ação, devido a um erro no código do formulário."
  
Quando estiver depurando:
  
Foco será movido para a linha de código no editor de código que está chamando o membro que requer confiança total, e a seguinte mensagem será exibida: **"SecurityException** não foi tratada pelo código de usuário - falha na solicitação". 
  
Para permitir que a lógica de negócios do modelo de formulário chamar esse membro quando ele estiver sendo depurados ou visualizados, você deve definir o nível de segurança do modelo de formulário como **Confiança total** conforme descrito no procedimento a seguir. 
  
## <a name="configuring-a-managed-code-form-template-that-requires-full-trust"></a>Configurando um modelo de formulário de código gerenciado que requer confiança total

### <a name="set-your-forms-security-level-to-full-trust"></a>Definir o nível de segurança do seu formulário como confiança total

1. No InfoPath, abra o modelo de formulário no modo de design.
    
2. Clique na guia **arquivo** e clique em **Opções de formulário** , na guia **informações** . 
    
3. Na lista **categoria** , clique em **Security e Trust.**
    
4. Em **Nível de segurança**, desmarque a **determinar o nível de segurança automaticamente**.
    
5. Selecione a **Confiança total**e clique em **Okey**.
    
Depois que esse procedimento é executado, você pode depurar seu projeto, conforme descrito em [Visualizar e depurar modelos de formulário do InfoPath com código](how-to-preview-and-debug-infopath-form-templates-with-code.md).
  
> [!NOTE]
> Implantando com êxito um modelo de formulário de código gerenciado que requer confiança total requer etapas adicionais, como assinar digitalmente, ou instalar e registrar o modelo de formulário. Para obter informações sobre como implantar um modelo de formulário de código gerenciado depois que ele é depurado ver, [Implantar modelos de formulário do InfoPath com código](how-to-deploy-infopath-form-templates-with-code.md). 
  
## <a name="see-also"></a>Confira também



[Visualizar e depurar modelos de formulário do InfoPath com código](how-to-preview-and-debug-infopath-form-templates-with-code.md)
  
[Implantar modelos de formulário do InfoPath com código](how-to-deploy-infopath-form-templates-with-code.md)

