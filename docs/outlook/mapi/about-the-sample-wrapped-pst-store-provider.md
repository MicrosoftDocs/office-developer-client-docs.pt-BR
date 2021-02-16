---
title: Sobre o provedor de armazenamento PST com conteúdo de exemplo
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 953391ce-31a2-3271-365a-284cf5e15d82
description: 'Last modified: July 03, 2012'
ms.openlocfilehash: 779dd96c4f07c0c5eee60ae046cd17db98eebfd9
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33432720"
---
# <a name="about-the-sample-wrapped-pst-store-provider"></a>Sobre o provedor de armazenamento PST com conteúdo de exemplo

 
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
## <a name="overview-of-message-store-providers"></a>Visão geral dos provedores de armazenamento de mensagens

Os provedores de armazenamento de mensagens lidam com o armazenamento e a recuperação de mensagens e outras informações para os usuários de aplicativos cliente. As informações da mensagem são organizadas usando um sistema hierárquico conhecido como armazenamento de mensagens. O armazenamento de mensagens é implementado em vários níveis, com contêineres chamados pastas que armazenam mensagens de diferentes tipos. Não há limite para o número de níveis em um armazenamento de mensagens; podem conter muitas subpastas.
  
Os dados do armazenamento de mensagens podem ser usados de várias maneiras. Além do uso típico de email, as pastas podem ser usadas como um fórum para discussão pública, como um repositório para documentos de referência ou como um contêiner para informações de quadro de boletins. Um único armazenamento de mensagens pode conter vários tipos de informações, alguns modificáveis e outros não. Vários clientes podem instalar o mesmo armazenamento de mensagens, tornando fácil e rápido o compartilhamento de dados.
  
As pastas do armazenamento de mensagens permitem classificar e filtrar mensagens e personalizar a exibição em uma exibição da interface do usuário. Links para mensagens filtradas são mantidos em pastas especiais chamadas pastas de resultados de pesquisa. O usuário de um aplicativo cliente insira critérios de filtragem, a que o MAPI se refere como uma restrição, e os critérios são aplicados às mensagens armazenadas em uma ou mais pastas. Por exemplo, um usuário pode querer exibir apenas as mensagens que lidam com um assunto específico com datas de chegada mais recentes do que a semana anterior. As referências às mensagens que corresponderem aos critérios são listadas na pasta de resultados da pesquisa e as mensagens reais permanecem em suas pastas regulares.
  
As mensagens são as unidades de dados transferidos de um usuário ou aplicativo para outro usuário ou aplicativo. Cada mensagem contém algumas informações de texto e envelope de mensagem usadas para transmissão. Algumas mensagens incluem um ou mais anexos ou dados adicionais relacionados a e transportadas com uma mensagem na forma de um arquivo, outra mensagem ou um objeto OLE.
  
## <a name="the-sample-wrapped-pst-store-provider"></a>O exemplo de provedor de armazenamento PST com conteúdo

A API de Replicação permite replicar itens de um repositório de dados back-end para um repositório PST do Outlook. Use a API de Replicação para replicar os dados em um armazenamento PST dedicado e acompanhar o estado de sincronização. Essa abordagem não exige que você apresente um provedor de armazenamento MAPI personalizado, que é complexo de gravação e manutenção. No entanto, o provedor de armazenamento PST não precisa ser empacotado para trabalhar com a API de Replicação.
  
O Provedor de Armazenamento PST com Conteúdo de Exemplo usa o provedor de arquivos de Pastas Particulares (PST) como back-end para armazenar dados. O provedor de armazenamento PST empacotado deve ser usado em conjunto com a API de Replicação. Para obter mais informações, consulte [Sobre a API de replicação.](about-the-replication-api.md) A maioria das funções no Provedor de Armazenamento PST com Fim de Exemplo passa seus argumentos diretamente para o provedor de PST subjacente. Determinadas funções exigem implementação especial e são descritas nos tópicos a seguir.
  
## <a name="in-this-section"></a>Nesta seção

- [Instalando o provedor de armazenamento PST com conteúdo de exemplo](installing-the-sample-wrapped-pst-store-provider.md)
    
- Explica como baixar e instalar o Sample Wrapped PST Store Provider.
    
- [Inicializando um provedor de armazenamento PST empacotado](initializing-a-wrapped-pst-store-provider.md)
    
- A primeira etapa na implementação de um provedor de armazenamento PST empacotado é inicializar e configurar o provedor de armazenamento PST empacotado.
    
- [Logondo em um provedor de armazenamento PST empacotado](logging-on-to-a-wrapped-pst-store-provider.md)
    
- Depois que um provedor de armazenamento PST empacotado for inicializado, você deverá implementar funções para que o MAPI e o spooler MAPI possam fazer logoff no provedor de armazenamento PST empacotado.
    
- [Usando um provedor de armazenamento PST empacotado](using-a-wrapped-pst-store-provider.md)
    
- Para usar um provedor de armazenamento PST empacotado, você deve quebrar a interface **[IMAPISupport::IUnknown](imapisupportiunknown.md)** para implementar tarefas comuns do provedor de armazenamento PST. 
    
- [Desligar um provedor de armazenamento PST empacotado](shutting-down-a-wrapped-pst-store-provider.md)
    
- Depois de terminar de usar um provedor de armazenamento PST empacotado, você deve desligar corretamente o provedor de armazenamento PST empacotado.
    
## <a name="see-also"></a>Confira também



[Sobre a API de replicação](about-the-replication-api.md)
  
[Desenvolver um provedor de repositórios de mensagens MAPI](developing-a-mapi-message-store-provider.md)

