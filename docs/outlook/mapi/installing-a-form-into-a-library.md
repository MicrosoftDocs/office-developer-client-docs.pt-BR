---
title: Instalar um formulário em uma biblioteca
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 303c9dcb-f9b5-4cea-b5f2-3eba01aa3b09
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 08470a80153e42136922ae502252d83de0125512
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33433140"
---
# <a name="installing-a-form-into-a-library"></a>Instalar um formulário em uma biblioteca

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
O Gerenciador de formulários MAPI padrão fornecido com o Windows SDK não fornece uma interface de usuário para a instalação de formulários nas várias bibliotecas de formulários. Por isso, você precisará criar um pequeno aplicativo — ou um conjunto detalhado de instruções, que os usuários podem usar para instalar o formulário.
  
Se você implementar um aplicativo de instalação, a série de ações que ele deve executar para instalar um formulário em uma tabela de conteúdo associada da pasta é a seguinte:
  
1. Chame a função [MAPIOpenFormMgr](mapiopenformmgr.md) para abrir o Gerenciador de formulários. 
    
2. Use [IMAPIFormMgr:: OpenFormContainer](imapiformmgr-openformcontainer.md) ou [IMAPIFormMgr:: SelectFormContainer](imapiformmgr-selectformcontainer.md) método para selecionar e abrir o contêiner de destino para o formulário. 
    
3. Use a função [IMAPIFormContainer:: InstallForm](imapiformcontainer-installform.md) para instalar o formulário. 
    
    As etapas 4 a 6 são para instalação em uma biblioteca de formulários local:
    
4. Copie todos os arquivos para o local apropriado no disco local, se a instalação for para a biblioteca de formulários local na estação de trabalho do usuário. Se necessário, modifique o arquivo de configuração de formulário para refletir os caminhos atuais dos componentes. O arquivo de configuração de formulário pode conter caminhos relativos, caso em que esta etapa pode não ser necessária.
    
5. Conclua as etapas de registro OLE apropriadas para associar o tipo de mensagem ao servidor de formulário que está sendo instalado.
    
6. Se o formulário foi instalado na biblioteca de formulários local, copie os arquivos de ícone (. ico) e de configuração (. cfg) do formulário para o diretório%WINDOWS%\FORMS\CONFIGS para que o formulário possa ser restaurado automaticamente caso a biblioteca de formulários esteja corrompida ou excluída. Esta etapa é recomendada, mas não obrigatória.
    
> [!NOTE]
> Você pode simplificar a instalação em uma biblioteca de formulários local, substituindo as etapas 1 e 2 por uma chamada para a função [MAPIOpenLocalFormContainer](mapiopenlocalformcontainer.md) . 
  
## <a name="see-also"></a>Confira também



[Desenvolver servidores de formulário MAPI](developing-mapi-form-servers.md)

