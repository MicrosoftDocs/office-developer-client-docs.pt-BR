---
title: Sobre o exemplo de provedor de repositório PST encapsulado
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 953391ce-31a2-3271-365a-284cf5e15d82
description: 'Última modificação: 03 de julho de 2012'
ms.openlocfilehash: 779dd96c4f07c0c5eee60ae046cd17db98eebfd9
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33432720"
---
# <a name="about-the-sample-wrapped-pst-store-provider"></a>Sobre o exemplo de provedor de repositório PST encapsulado

 
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
## <a name="overview-of-message-store-providers"></a>Visão geral dos provedores de repositório de mensagens

Os provedores de repositórios de mensagens lidam com o armazenamento e a recuperação de mensagens e outras informações para os usuários de aplicativos cliente. As informações da mensagem são organizadas usando um sistema hierárquico conhecido como repositório de mensagens. O repositório de mensagens é implementado em vários níveis, com contêineres chamados pastas que armazenam mensagens de tipos diferentes. Não há limite para o número de níveis em um repositório de mensagens; as pastas podem conter muitas subpastas.
  
Os dados do repositório de mensagens podem ser usados de várias maneiras. Além do uso de email típico, as pastas podem ser usadas como um fórum para discussão pública, como um repositório para documentos de referência ou como um contêiner para informações de BBS. Um único repositório de mensagens pode conter vários tipos de informações, alguns e outros não. Vários clientes podem instalar o mesmo armazenamento de mensagens, tornando mais fácil e rápido compartilhar dados.
  
As pastas de repositório de mensagens permitem que você classifique e Filtre mensagens e personalize o modo de exibição em uma interface de usuário (UI). Links para mensagens filtradas são mantidos em pastas especiais chamadas de resultados de pesquisa. O usuário de um aplicativo cliente insere critérios de filtragem, aos quais o MAPI se refere como uma restrição, e os critérios são aplicados às mensagens armazenadas em uma ou mais pastas. Por exemplo, um usuário pode querer exibir apenas as mensagens que lidam com um assunto específico com datas de chegada mais recentes do que a semana passada. As referências às mensagens que correspondem aos critérios são listadas na pasta de resultados de pesquisa e as mensagens reais permanecem em suas pastas regulares.
  
As mensagens são unidades de dados transferidas de um usuário ou aplicativo para outro usuário ou aplicativo. Cada mensagem contém algumas informações de texto e envelope de mensagem que são usadas para transmissão. Algumas mensagens incluem um ou mais anexos ou dados adicionais relacionados a e transportados com uma mensagem no formato de um arquivo, outra mensagem ou um objeto OLE.
  
## <a name="the-sample-wrapped-pst-store-provider"></a>O exemplo de provedor de repositório PST encapsulado

A API de replicação permite que você replique itens de um repositório de dados de back-end para um repositório de PST do Outlook. Use a API de replicação para replicar os dados em um repositório PST dedicado e manter o controle do estado de sincronização. Essa abordagem não exige que você apresente um provedor de armazenamento MAPI personalizado, que é complexo para gravar e manter. No enTanto, o provedor do repositório PST precisa ser encapsulado para trabalhar com a API de replicação.
  
O exemplo de provedor de repositório PST encapsulado usa o arquivo de pastas particulares (PST) como back-end para armazenar dados. O provedor de repositório PST encapsulado deve ser usado em conjunto com a API de replicação. Para obter mais informações, consulte [sobre a API de replicação](about-the-replication-api.md). A maioria das funções no provedor de repositório PST encapsulado de amostra passam seus argumentos diretamente para o provedor de PST subjacente. Determinadas funções exigem implementação especial e são descritos nos tópicos a seguir.
  
## <a name="in-this-section"></a>Nesta seção

- [Instalando o provedor de repositório PST encapsulado de exemplo](installing-the-sample-wrapped-pst-store-provider.md)
    
- Explica como baixar e instalar o exemplo de provedor de repositório PST encapsulado.
    
- [Inicializando um provedor de repositório PST encapsulado](initializing-a-wrapped-pst-store-provider.md)
    
- A primeira etapa na implementação de um provedor de repositório PST encapsulado é inicializar e configurar o provedor de repositório PST encapsulado.
    
- [Fazer logon em um provedor de repositório PST encapsulado](logging-on-to-a-wrapped-pst-store-provider.md)
    
- Após a inicialização de um provedor de repositório PST encapsulado, você deve implementar as funções para que o MAPI e o spooler MAPI possam fazer logon no provedor de repositório PST encapsulado.
    
- [Usando um provedor de repositório PST encapsulado](using-a-wrapped-pst-store-provider.md)
    
- Para usar um provedor de repositório PST encapsulado, você deve encapsular a interface **[IMAPISupport:: IUnknown](imapisupportiunknown.md)** para implementar tarefas comuns do provedor de repositório PST encapsulado. 
    
- [DesLigamento de um provedor de repositório PST encapsulado](shutting-down-a-wrapped-pst-store-provider.md)
    
- Após concluir o uso de um provedor de repositório PST encapsulado, você deve desligar corretamente o provedor de repositório PST encapsulado.
    
## <a name="see-also"></a>Confira também



[Sobre a API de replicação](about-the-replication-api.md)
  
[Desenvolver um provedor de repositórios de mensagens MAPI](developing-a-mapi-message-store-provider.md)

