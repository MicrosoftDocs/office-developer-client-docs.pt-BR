---
title: Pastas de recebimento MAPI
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 2e1287a3-0f15-4d9a-b7ee-738fce9cd51f
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: b22b8641d55037d3755fc9ae32b97455223bbd12
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32329754"
---
# <a name="mapi-receive-folders"></a>Pastas de recebimento MAPI

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Uma pasta de recebimento mantém mensagens de entrada de uma determinada classe de mensagem. As associações de pastas de recebimento podem ser estabelecidas por clientes, pelo provedor de armazenamento de mensagens ou por MAPI. O MAPI tem duas pastas de recebimento padrão: a pasta raiz do repositório de mensagens e a pasta caixa de entrada da subárvore de mensagens interpessoais (IPM). A pasta raiz do repositório de mensagens é a pasta de recebimento padrão para todas as mensagens de comunicação entre processos (IPC).
  
 A pasta caixa de entrada é criada por MAPI para cada novo repositório de mensagens e atua como a pasta de recebimento padrão para as seguintes classes de mensagens: 
  
- A classe de mensagem IPM.
    
- A classe de mensagem de relatório.
    
- Uma classe vazia, ou ausente.
    
Todas as mensagens de relatório, mesmo aquelas enviadas em resposta a uma mensagem de IPC, são colocadas na pasta caixa de entrada. Os aplicativos de cliente IPC que processam seus próprios relatórios devem adicionar explicitamente uma pasta de recebimento para a classe de relatório específica. Por exemplo, se um cliente espera receber mensagens com o IPC de classe. Paper. Order, ele deve chamar o método [IMsgStore:: SetReceiveFolder](imsgstore-setreceivefolder.md) para estabelecer uma pasta de recebimento para relatórios com o relatório de classe. IPC. Paper. Order. 
  
As associações de pastas de recebimento são baseadas na organização hierárquica das classes de mensagem. Os clientes podem estabelecer explicitamente uma associação entre uma pasta de recebimento e uma classe de mensagem ou usar as pastas de recebimento padrão MAPI. Normalmente, os clientes designam uma pasta para receber mensagens de uma classe base e todas as suas subclasses. Por exemplo, um cliente típico estabeleceria uma associação para mensagens com a classe **MyClass**. Em seguida, se o cliente recebeu mensagens com classes **MyClass. Home** ou **MyClass. home. doméstico**, essas mensagens vão para a pasta de recebimento da classe base, **MyClass**.
  
Há três métodos de armazenamento de mensagens que os clientes usam para trabalhar com pastas de recebimento:
  
- [IMsgStore::GetReceiveFolderTable](imsgstore-getreceivefoldertable.md)
    
- [IMsgStore::GetReceiveFolder](imsgstore-getreceivefolder.md)
    
- [IMsgStore::SetReceiveFolder](imsgstore-setreceivefolder.md)
    
A tabela de pastas de recebimento é uma listagem de informações sobre todas as pastas de recebimento estabelecidas para um repositório de mensagens. Seu conjunto de colunas obrigatório inclui a classe de mensagem, a chave de registro e o identificador de entrada.
  
Para recuperar uma pasta de recebimento para uma determinada classe de mensagem, os clientes passam a cadeia de caracteres de classe de mensagem para o método [IMsgStore:: GetReceiveFolder](imsgstore-getreceivefolder.md) . O provedor de repositório de mensagens retorna um identificador de entrada para a pasta correspondente. Para implementar o **GetReceiveFolder**, um provedor de repositório de mensagens deve usar um algoritmo que seleciona a pasta cuja classe de mensagens associada corresponde ao prefixo mais longo possível da classe de mensagem especificada. Por exemplo, suponha que o repositório de mensagens tenha as seguintes associações entre as pastas de recebimento e as classes de mensagens em sua tabela de pastas de recebimento:
  
- As mensagens **IPM** são colocadas na pasta caixa de entrada. 
    
- **IPM. Observação.** as mensagens de exemplo são colocadas na pasta Samples. 
    
A tabela a seguir mostra como as mensagens com várias classes seriam encaminhadas para a pasta de recebimento apropriada.
  
|**Classe de mensagens de entrada**|**Pasta receber**|
|:-----|:-----|
|**IPM. Note. Sample. Simple** <br/> |Pasta de exemplos  <br/> |
|**IPM. Observação** <br/> |Pasta caixa de entrada  <br/> |
|**IPM. Cartão de um** <br/> |Pasta caixa de entrada  <br/> |
|**IPM. Observação. Sample. Simple. totalmente** <br/> |Pasta de exemplos  <br/> |
   
Os clientes chamam o método **SetReceiveFolder** para fazer uma associação explícita entre uma determinada classe de mensagem e receber a pasta. Quando uma mensagem é entregue a uma classe de mensagem vazia, o MAPI coloca a mensagem na pasta Receive que é definida para um prefixo da classe vazia. Por exemplo, se o cliente tiver uma pasta de recebimento estabelecida para mensagens com a classe **IPM** e uma mensagem com classe **IPM. Note. Test** for entregue, esta mensagem será colocada na pasta receber da classe de mensagem **IPM** . 
  
Na chamada de **SetReceiveFolder**, os clientes normalmente passam uma cadeia de caracteres de classe de mensagem e o identificador de entrada da nova pasta de recebimento. No enTanto, os clientes podem passar NULL para um ou ambos os parâmetros. A tabela a seguir descreve o comportamento que resulta da especificação de NULL para a classe de mensagem e os parâmetros de identificador de entrada. 
  
|**Parâmetro _SetReceiveFolder_**|**Comportamento resultante**|
|:-----|:-----|
|Identificador de entrada definido como nulo  <br/> |O repositório de mensagens exclui a associação entre a classe de mensagem especificada e sua pasta de recebimento existente. Uma nova pasta de recebimento não é estabelecida.  <br/> Chamadas subsequentes para **GetReceiveFolder** com esta classe de mensagem retornarão a pasta de recebimento para um prefixo da classe de mensagem; para novos repositórios de mensagens, **GetReceiveFolder** retornará a caixa de entrada na subárvore IPM.  <br/> |
|Classe de mensagem definida como NULL  <br/> |O repositório de mensagens altera a associação da classe de mensagens vazia para a pasta indicada. As mensagens de entrada cuja classe é, de outra forma, não reconhecidas vão para esta pasta.  <br/> |
|Identificador de entrada e classe de mensagem definidos como nulos  <br/> |O repositório de mensagens exclui a associação de classe/pasta da classe de mensagem vazia. Você não deve definir ambos os parâmetros como nulo, porque normalmente resulta em mensagens de entrada sendo colocadas na pasta raiz do repositório de mensagens, uma pasta invisível para o cliente.  <br/> |
   
Embora a classe de uma mensagem nunca deva estar vazia, uma classe de mensagem vazia pode ocorrer. É responsabilidade do repositório de mensagens atribuir a classe de mensagem a **IPM** para novas mensagens de saída que têm uma classe vazia; é responsabilidade do provedor de transporte atribuir **IPM. Observe** como a classe para mensagens de entrada que têm qualquer classe vazia. 
  
## <a name="see-also"></a>Confira também



[Pastas MAPI](mapi-folders.md)

