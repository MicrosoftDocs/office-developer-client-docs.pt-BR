---
title: MAPI recebem pastas
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 2e1287a3-0f15-4d9a-b7ee-738fce9cd51f
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 619bd2d5e3b40e49da835d774035ba237af06699
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19767916"
---
# <a name="mapi-receive-folders"></a>MAPI recebem pastas

  
  
**Aplica-se a**: Outlook 
  
Uma pasta de recebimento contém mensagens de entrada de uma classe de mensagem específica. Associações podem ser estabelecidas pelos clientes, o provedor de armazenamento de mensagem ou MAPI de pasta de recebimento. MAPI tem dois padrão recebem pastas: a pasta raiz do armazenamento de mensagens e da pasta de caixa de entrada da subárvore interpessoais mensagens (IPM). A pasta raiz do armazenamento de mensagens é o padrão receber a pasta para todas as mensagens de comunicação entre processos (CPI).
  
 A pasta de caixa de entrada é criada pelo MAPI para cada novo armazenamento de mensagens e atua como o padrão recebe a pasta para as classes de mensagem a seguir: 
  
- A classe de mensagem IPM.
    
- A classe de mensagem do relatório.
    
- Uma classe vazia ou ausente.
    
Todas as mensagens de relatório, mesmo aqueles enviado em resposta a uma mensagem de CPI, são colocadas na pasta caixa de entrada. Aplicativos de cliente CPI que processar seus próprios relatórios deverá adicionar explicitamente uma pasta de recebimento para a classe específica do relatório. Por exemplo, se um cliente espera receber mensagens com a classe CPI. Paper.Order, ele deve chamar o método [IMsgStore::SetReceiveFolder](imsgstore-setreceivefolder.md) para estabelecer uma pasta de recebimento de relatórios com a classe Report.IPC.Paper.Order. 
  
Receba a pasta associações baseiam-se na organização hierárquica de classes de mensagem. Os clientes podem estabelecer uma associação entre uma pasta de recebimento e uma classe de mensagem ou usar as pastas de recebimento padrão MAPI explicitamente. Normalmente, os clientes designar uma pasta para receber mensagens para uma classe de base e todas as suas subclasses. Por exemplo, um cliente típico seria estabelecer uma associação para mensagens com a classe **MyClass**. Em seguida, se o cliente tiver recebido mensagens com classes **MyClass.Home** ou **MyClass.Home.Kitchen.Computer**, essas mensagens iria para a pasta de recebimento para a classe de base, **MyClass**.
  
Há três mensagem métodos repositório que são usadas pelos clientes para trabalhar com pastas de receber:
  
- [IMsgStore::GetReceiveFolderTable](imsgstore-getreceivefoldertable.md)
    
- [IMsgStore::GetReceiveFolder](imsgstore-getreceivefolder.md)
    
- [IMsgStore::SetReceiveFolder](imsgstore-setreceivefolder.md)
    
A tabela de pasta de recebimento é uma listagem das informações sobre todas as pastas de recebimento estabelecidas para um armazenamento de mensagens. Seu conjunto de coluna necessária inclui a classe de mensagem, chave de registro e o identificador de entrada.
  
Para recuperar uma pasta de recebimento para uma classe de mensagem específica, clientes passam a cadeia de caracteres de classe de mensagem para o método [IMsgStore::GetReceiveFolder](imsgstore-getreceivefolder.md) . A mensagem armazene o provedor retorna um identificador de entrada para a pasta correspondente. Para implementar **GetReceiveFolder**, um provedor de armazenamento de mensagem deve usar um algoritmo que seleciona a pasta cujo classe de mensagem associada coincide com o prefixo mais longo possível da classe de mensagem especificado. Por exemplo, suponha que o armazenamento de mensagens tem as seguintes associações entre recebem pastas e mensagens classes em sua tabela de pasta de recebimento:
  
- Mensagens **IPM** são colocadas na pasta caixa de entrada. 
    
- **IPM. Note.Sample** mensagens são colocadas na pasta Samples. 
    
A tabela a seguir mostra como mensagens com várias classes serão encaminhadas para o apropriado a pasta de recebimento.
  
|**Classe de mensagem de entrada**|**Pasta de recebimento**|
|:-----|:-----|
|**IPM. Note.Sample.Simple** <br/> |Pasta de amostras  <br/> |
|**IPM. Observação** <br/> |Pasta caixa de entrada  <br/> |
|**IPM. Cartão de ponto** <br/> |Pasta caixa de entrada  <br/> |
|**IPM. Note.Sample.Simple.Totally** <br/> |Pasta de amostras  <br/> |
   
Clientes chame o método de **SetReceiveFolder** para fazer uma associação explícita entre uma classe de mensagem específica e a pasta de recebimento. Quando uma mensagem é entregue a uma classe de mensagem vazia, o MAPI coloca a mensagem na pasta de recebimento que foi definida para um prefixo da classe vazia. Por exemplo, se seu cliente tiver uma pasta de recebimento estabelecida para mensagens com classes **IPM** e uma mensagem com a classe **IPM. Note. Test** é entregue, esta mensagem será colocada na pasta de recebimento para a classe de mensagem **IPM** . 
  
Em chamar **SetReceiveFolder**, os clientes normalmente passam uma cadeia de caracteres de classe de mensagem e o identificador de entrada da nova pasta de recebimento. No entanto, os clientes podem passar NULL devido a um ou ambos os parâmetros. A tabela a seguir descreve o comportamento que resulta da especificação NULL para os parâmetros de identificador de classe e entrada de mensagem. 
  
|**Parâmetro _SetReceiveFolder_**|**Comportamento resultante**|
|:-----|:-----|
|Identificador de entrada definido como NULL  <br/> |O armazenamento de mensagens exclui a associação entre especificado a existente e a classe de pasta de recebimento de mensagem. Receber uma nova pasta não é estabelecida.  <br/> As chamadas subsequentes com essa classe de mensagem para **GetReceiveFolder** retornará a pasta de recebimento de um prefixo da classe de mensagem; para repositórios de nova mensagem, **GetReceiveFolder** retornará a caixa de entrada na subárvore IPM.  <br/> |
|Classe de mensagem definido como NULL  <br/> |O armazenamento de mensagens altera a associação para a classe de mensagem vazia na pasta indicada. Mensagens de entrada cujo classe contrário é reconhecido irão para essa pasta.  <br/> |
|O identificador de entrada e a classe de mensagem definido como NULL  <br/> |O armazenamento de mensagens exclui a associação de classe/pasta para a classe de mensagem vazia. Você não deve definir ambos os parâmetros como NULL, porque geralmente resulta em mensagens de entrada que está sendo colocadas na pasta raiz do armazenamento de mensagens, uma pasta que é invisível para o cliente.  <br/> |
   
Embora a classe da mensagem nunca deve estar vazio, uma classe de mensagem vazia pode ocorrer. É responsabilidade do armazenamento de mensagens para atribuir a classe de mensagem ao **IPM** para novas mensagens de saída que possuem uma classe vazia; é responsabilidade do provedor de transporte para atribuir **IPM. Observação** como a classe de mensagens de entrada que possuem qualquer classe vazia. 
  
## <a name="see-also"></a>Confira também



[Pastas MAPI](mapi-folders.md)

