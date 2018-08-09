---
title: Instalar um formulário em uma biblioteca
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 303c9dcb-f9b5-4cea-b5f2-3eba01aa3b09
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 54b2dece31937b1ff233d4d1e7d8bbc198bfe118
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19767574"
---
# <a name="installing-a-form-into-a-library"></a>Instalar um formulário em uma biblioteca

  
  
**Aplica-se a**: Outlook 
  
O Gerenciador de formulário MAPI padrão fornecido com o SDK do Windows não fornece uma interface de usuário de instalação formulários nas várias bibliotecas de formulário. Dessa forma, você precisará criar um aplicativo pequeno — ou detalhados de conjunto de instruções — que os usuários podem usar para instalar o formulário.
  
Se você implementar um aplicativo de instalação, a série de ações ele deve executar para instalar um formulário em associado conteúdo de uma pasta tabela são os seguintes:
  
1. Chame a função de [MAPIOpenFormMgr](mapiopenformmgr.md) para abrir o formulário manager. 
    
2. Use o método [IMAPIFormMgr::OpenFormContainer](imapiformmgr-openformcontainer.md) ou [IMAPIFormMgr::SelectFormContainer](imapiformmgr-selectformcontainer.md) para selecionar e abrir o contêiner de destino para o formulário. 
    
3. Use a função [IMAPIFormContainer::InstallForm](imapiformcontainer-installform.md) para instalar o formulário. 
    
    As etapas 4 a 6 são para instalação em uma biblioteca de formulários local:
    
4. Copie todos os arquivos para o local apropriado no disco local, se a instalação é a biblioteca de formulários local na estação de trabalho do usuário. Se necessário, modifique o arquivo de configuração de formulário para refletir o atuais caminhos dos componentes. O arquivo de configuração de formulário pode conter caminhos relativos, caso em que esta etapa talvez não seja necessária.
    
5. Conclua as etapas apropriadas de registro OLE para associar o tipo de mensagem com o servidor de formulário que está sendo instalado.
    
6. Se o formulário foi instalado na biblioteca de formulários local, copie o ícone (. ico) do formulário e arquivos de configuração (. cfg) no diretório %WINDOWS%\FORMS\CONFIGS para que o formulário possa ser restaurado automaticamente caso a biblioteca de formulários está corrompida ou excluída. Esta etapa é recomendado, mas não seja obrigatório.
    
> [!NOTE]
> Você pode simplificar a instalação em uma biblioteca de formulários locais, substituindo as etapas 1 e 2 por uma chamada para a função [MAPIOpenLocalFormContainer](mapiopenlocalformcontainer.md) . 
  
## <a name="see-also"></a>Confira também



[Desenvolver servidores de formulário MAPI](developing-mapi-form-servers.md)

