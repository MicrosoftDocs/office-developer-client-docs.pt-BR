---
title: Sobre a amostra quebradas provedor de repositórios de PST
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 953391ce-31a2-3271-365a-284cf5e15d82
description: 'Modificado pela última vez: 03 de julho de 2012'
ms.openlocfilehash: 51aef9d8778997749e401b008ebdb4126a248ee0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19766097"
---
# <a name="about-the-sample-wrapped-pst-store-provider"></a>Sobre a amostra quebradas provedor de repositórios de PST

 
  
**Aplica-se a**: Outlook 
  
## <a name="overview-of-message-store-providers"></a>Visão geral dos provedores de armazenamento de mensagens

Provedores de armazenamento de mensagem lidar com o armazenamento e a recuperação de mensagens e outras informações para os usuários de aplicativos do cliente. As informações da mensagem são organizadas por meio de um sistema hierárquico conhecido como um armazenamento de mensagens. O armazenamento de mensagens é implementado em vários níveis, com chamadas pastas que armazenam mensagens de diferentes tipos de contêineres. Não há nenhum limite no número de níveis em um armazenamento de mensagem. pastas podem conter muitas subpastas.
  
Dados do repositório de mensagens podem ser usados em uma variedade de formas. O uso de email típica, além de pastas podem ser usadas como um fórum de discussão pública, como um repositório de documentos de referência ou como um contêiner para obter informações de quadro de avisos. Um repositório de mensagem única pode conter vários tipos de informação, alguns modificável e alguns não. Vários clientes podem instalar o mesmo armazenamento de mensagens, tornando fácil e rápida para compartilhar dados.
  
Pastas do repositório de mensagens permitem que você deve classificar e filtrar mensagens e personalizar o modo de exibição em uma exibição do usuário (UI) da interface. Links para mensagens filtradas são mantidos nas pastas especiais chamadas de pastas de resultados de pesquisa. O usuário de um aplicativo cliente insere os critérios de filtragem, que MAPI se refere a como uma restrição, e os critérios é aplicado às mensagens armazenadas em pastas de um ou mais. Por exemplo, um usuário talvez queira exibir somente as mensagens lidando com um determinado assunto com datas de chegada que são mais recente do que a última semana. Referências para as mensagens que correspondem aos critérios são listadas na pasta resultados de pesquisa e as mensagens reais permanecem em suas pastas regulares.
  
As mensagens são as unidades de dados transferidos de um usuário ou aplicativo para outro usuário ou aplicativo. Cada mensagem contém alguns texto da mensagem e informações de envelope de mensagem que são usadas para a transmissão. Algumas mensagens incluem um ou mais anexos ou dados adicionais relacionadas a e transportados com uma mensagem na forma de um arquivo, outra mensagem ou um objeto OLE.
  
## <a name="the-sample-wrapped-pst-store-provider"></a>O exemplo de provedor de repositórios de PST quebrado automaticamente

A API de replicação permite que você replique os itens de um repositório de dados back-end em um armazenamento de PST do Outlook. Você pode usar a API de replicação para replicar os dados para um repositório de PST dedicado e controlar o estado de sincronização. Essa abordagem não exige que você apresentar um provedor de repositório MAPI personalizado, que é complexo para escrever e manter. No entanto, o provedor de repositórios de PST precisa ser quebradas para trabalhar com a API de replicação.
  
O provedor de armazenamento de PST quebrado automaticamente do exemplo usa o provedor de pastas particulares (. PST) do arquivo como back-end para armazenar os dados. O provedor de repositórios de PST com quebra deve ser usado em conjunto com a API de replicação. Para obter mais informações, consulte [Sobre o API de replicação](about-the-replication-api.md). A maioria das funções do provedor de armazenamento do exemplo quebradas PST passa seus argumentos diretamente para o provedor de PST subjacente. Determinadas funções exigem implementação especial e são descritas nos tópicos a seguir.
  
## <a name="in-this-section"></a>Nesta se��o

- [Instalação do exemplo quebrado automaticamente o provedor de armazenamento de PST](installing-the-sample-wrapped-pst-store-provider.md)
    
- Explica como baixar e instalar o provedor de repositórios de PST quebrado automaticamente amostra.
    
- [Inicializar um provedor de repositório PST encapsulado](initializing-a-wrapped-pst-store-provider.md)
    
- A primeira etapa na implementação de um provedor de armazenamento de PST com quebra é inicializar e configurar o provedor de repositórios de PST com quebra.
    
- [Fazer logon no provedor de um repositório PST encapsulado](logging-on-to-a-wrapped-pst-store-provider.md)
    
- Depois que um provedor de armazenamento de PST com quebra é inicializado, você deve implementar funções para que o spooler MAPI e MAPI podem fazer logon no provedor de armazenamento de PST com quebra.
    
- [Usando um provedor de repositório PST encapsulado](using-a-wrapped-pst-store-provider.md)
    
- Para usar um repositório PST encapsulado provedor que você deve quebrar a interface **[IMAPISupport::IUnknown](imapisupportiunknown.md)** implementar comuns quebradas tarefas do provedor de armazenamento de PST. 
    
- [Encerrando um provedor de repositório PST encapsulado](shutting-down-a-wrapped-pst-store-provider.md)
    
- Após concluir o uso de um provedor de armazenamento com quebra PST, você deve desligar corretamente o provedor de repositórios de PST com quebra.
    
## <a name="see-also"></a>Confira também



[Sobre a API de replicação](about-the-replication-api.md)
  
[Desenvolvendo um provedor de armazenamento de mensagens MAPI](developing-a-mapi-message-store-provider.md)

