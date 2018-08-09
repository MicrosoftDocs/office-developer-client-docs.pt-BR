---
title: ADRPARM
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ADRPARM
api_type:
- COM
ms.assetid: 35cd57b4-9901-456c-bf06-1f84e274eb4e
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: ad26cb9b77404d6470f7a8d787eb85edc5cce402
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/21/2018
ms.locfileid: "19766159"
---
# <a name="adrparm"></a>ADRPARM

**Aplica-se a**: Outlook 
  
Descreve a exibição e o comportamento da caixa de diálogo endereço comum. 
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |Mapidefs.h  <br/> |
   
```cpp
typedef struct _ADRPARM
{
  ULONG cbABContEntryID;
  LPENTRYID lpABContEntryID;
  ULONG ulFlags;
  LPVOID lpReserved;
  ULONG ulHelpContext;
  LPSTR lpszHelpFileName;
  LPFNABSDI lpfnABSDI;
  LPFNDISMISS lpfnDismiss;
  LPVOID lpvDismissContext;
  LPSTR lpszCaption;
  LPSTR lpszNewEntryTitle;
  LPSTR lpszDestWellsTitle;
  ULONG cDestFields;
  ULONG nDestFieldFocus;
  LPSTR FAR *lppszDestTitles;
  ULONG FAR *lpulDestComps;
  LPSRestriction lpContRestriction;
  LPSRestriction lpHierRestriction;
} ADRPARM, FAR *LPADRPARM;

```

## <a name="members"></a>Members

**cbABContEntryID**
  
> Contagem de bytes no identificador de entrada apontado pela **lpABContEntryID**.
    
**lpABContEntryID**
  
> Ponteiro para o identificador de entrada do contêiner que fornece a lista inicial dos endereços de destinatário que são exibidos na caixa de diálogo endereço.
    
**ulFlags**
  
> Bitmask dos sinalizadores associados a várias opções de caixa de diálogo de endereço. Sinalizadores a seguir podem ser definidos:
    
AB_RESOLVE
  
> Habilite todos os nomes de ser resolvido depois que a caixa de diálogo de endereço é fechada. Se houver entradas ambíguas resultantes do processo de resolução de nome, uma caixa de diálogo é exibida avisar o usuário para obter ajuda na resolvê-los. Configuração esse sinalizador garante que todos os nomes retornados por [IAddrBook::Address](iaddrbook-address.md) forem resolvidos. 
    
AB_SELECTONLY
  
> Desabilite a criação de endereços únicos para uma lista de destinatários. Esse sinalizador é usado somente se a caixa de diálogo é modal, conforme indicado pelo sinalizador DIALOG_MODAL sendo definido.
    
ADDRESS_ONE
  
> O usuário pode selecionar exatamente um destinatário, em vez de vários destinatários de uma lista. Esse sinalizador é válido somente quando **cDestFields** é zero e a caixa de diálogo é modal, conforme indicado pelo sinalizador DIALOG_MODAL sendo definido. 
    
DIALOG_MODAL
  
> Faz com que a versão modal da caixa de diálogo endereço comum a ser exibido. Este sinalizador ou DIALOG_SDI deve ser definido; eles não podem ser definidos. 
    
DIALOG_OPTIONS
  
> Faz com que o botão de **Opções de enviar** a ser exibido na caixa de diálogo. Esse sinalizador é usado somente se a caixa de diálogo é modal, conforme indicado pelo sinalizador DIALOG_MODAL sendo definido. 
    
DIALOG_SDI
  
> Faz com que a versão sem janela restrita da caixa de diálogo endereço comum a ser exibido. Este sinalizador ou DIALOG_MODAL deve ser definido; eles não podem ser definidos. O sinalizador DIALOG_SDI é ignorado para clientes não são do Outlook e a versão modal da caixa de diálogo será exibida. Consequentemente, um ponteiro para uma alça não deverão ser esperado no parâmetro _lpulUIParam_ do [IAddrBook::Address](iaddrbook-address.md).
    
**lpReserved**
  
> Reservado, deve ser zero.
    
**ulHelpContext**
  
> Especifica o contexto dentro de **Ajuda** que será inicialmente exibido quando o usuário clica no botão Ajuda na caixa de diálogo endereço. 
    
**lpszHelpFileName**
  
> Ponteiro para o nome de um arquivo de Ajuda que será associado a caixa de diálogo de endereço. O membro **lpszHelpFileName** é usado em conjunto com **ulHelpContext** para chamar a função Windows **WinHelp** . 
    
**lpfnABSDI**
  
> Ponteiro para uma função MAPI com base no [ACCELERATEABSDI](accelerateabsdi.md) protótipo ou nulo. Este membro se aplica à versão sem janela restrita da caixa de diálogo apenas, conforme indicado pelo sinalizador DIALOG_SDI sendo definido. Clientes criando uma estrutura **ADRPARM** a serem passados para [IAddrBook::Address](iaddrbook-address.md) sempre devem definir o membro **lpfnABSDI** como NULL. Se o sinalizador DIALOG_SDI estiver definido, MAPI, em seguida, definirá-lo como uma função válida antes de retornar. Clientes chamar essa função em seu loop de mensagem para certificar-se de que os aceleradores no endereço do livro trabalho da caixa de diálogo. Quando a caixa de diálogo é fechada e MAPI chama a função apontada pelo membro **lpfnDismiss** , os clientes devem solte a função **ACCELERATEABSDI** seu do loop de mensagens. 
    
**lpfnDismiss**
  
> Ponteiro para uma função com base no [DISMISSMODELESS](dismissmodeless.md) protótipo ou nulo. Este membro se aplica somente à versão sem janela restrita da caixa de diálogo apenas, conforme indicado pelo sinalizador DIALOG_SDI sendo definido. MAPI chama a função **DISMISSMODELESS** quando o usuário descarte a caixa de diálogo sem janela restrita endereço informando um cliente chamar **IAddrBook::Address** que a caixa de diálogo não está mais ativa. 
    
**lpvDismissContext**
  
> Ponteiro para informações de contexto a serem passados para a função **DISMISSMODELESS** apontado pelo membro **lpfnDismiss** . Este membro só se aplica a versão sem janela restrita da caixa de diálogo, conforme indicado pelo sinalizador DIALOG_SDI sendo definido. 
    
**lpszCaption**
  
> Ponteiro para o texto a ser usado como o título para a caixa de diálogo endereço comuns.
    
**lpszNewEntryTitle**
  
> Ponteiro para o texto a ser usado como o rótulo do botão para o botão que invoca a caixa de diálogo **Nova entrada** ou outra caixa de diálogo. 
    
**lpszDestWellsTitle**
  
> Ponteiro para o texto a ser usado como um título para os controles de caixa de texto de destinatários que podem aparecer na versão modal da caixa de diálogo comum do endereço. Este membro não é usado para caixas de diálogo sem janela restrita. 
    
**cDestFields**
  
> Contagem de controles de caixa de texto de destinatário na versão modal de caixa de diálogo endereço ou zero se a caixa de diálogo não é modal. A caixa de diálogo de endereço está aberta para navegação somente quando as seguintes condições forem verdadeiras: 
    
  - O membro **cDestFields** é definido como zero. 
    
  - O sinalizador DIALOG_BOX está definido.
    
  - O sinalizador ADDRESS_ONE não estiver definido.
    
  A definição de **cDestFields** como 0XFFFFFFFF implica que MAPI deve criar o número padrão de texto destinatário controles da caixa. Nesse caso, os membros **lppszDestTitles** e **lpulDestComps** devem ser NULL. 
    
**nDestFieldFocus**
  
> Indica o controle de caixa de texto específico que deve ter o foco inicial quando a versão modal da caixa de diálogo aparece. Esse valor deve estar entre 0 e o valor da **cDestFields** menos 1. 
    
**lppszDestTitles**
  
> Ponteiro para uma matriz de rótulos de botões associados a cada um dos controles de caixa de texto que são exibidos na versão da caixa de diálogo endereço modal. O valor do membro **cDestFields** indica o número de rótulos incluídos na matriz. Se o membro **lppszDestTitles** for NULL, o método de **endereços** usa títulos padrão. 
    
**lpulDestComps**
  
> Ponteiro para uma matriz de valores de tipo de destinatário, como MAPI_TO, MAPI_CC e MAPI_BCC, que é associado a cada controle de caixa de texto. O valor do membro **CDestFields** indica o número de tipos de destinatários incluídos na matriz. Os valores apontados pela **lpulDestComps** podem ser usados para definir a propriedade **PR_RECIPIENT_TYPE** ([PidTagRecipientType](pidtagrecipienttype-canonical-property.md)) de cada destinatário. Se o membro **lpulDestComps** for NULL, o método de **endereços** usa os tipos de destinatário padrão. 
    
**lpContRestriction**
  
> Ponteiro para uma estrutura [SRestriction](srestriction.md) que limita o tipo de entradas de endereço que podem ser exibidos na caixa de diálogo. 
    
**lpHierRestriction**
  
> Ponteiro para uma estrutura **SRestriction** que limita os contêineres do catálogo de endereços que podem fornecer as entradas de endereço a ser exibido na caixa de diálogo. 
    
## <a name="remarks"></a>Comentários

Estruturas **ADRPARM** são usadas por clientes e provedores de serviços para controlar a aparência e o comportamento das caixas de diálogo de endereço comuns de MAPI. Existem duas variedades da caixa de diálogo endereço: sem janela restrita e modal. Alguns dos membros na estrutura **ADRPARM** aplicam às duas versões da caixa de diálogo, mas algumas só se aplicam a uma das duas versões. A tabela a seguir relaciona os membros de uma estrutura de **ADRPARM** para seu uso com caixas de diálogo comuns do endereço. 
  
|Membro ADRPARM|Tipo de caixa de diálogo|
|:-----|:-----|
|**cbABContEntryID** e **lpABContEntryID** <br/> |Janela restrita e sem janela restrita  <br/> |
|**ulFlags** <br/> |Janela restrita e sem janela restrita  <br/> |
|**lpReserved** <br/> |Janela restrita e sem janela restrita  <br/> |
|**ulHelpContext** e **lpszHelpFileName** <br/> |Janela restrita e sem janela restrita  <br/> |
|**lpfnABSDI** <br/> |Sem janela restrita  <br/> |
|**lpfnDismiss** e **lpvDismissContext** <br/> |Sem janela restrita  <br/> |
|**lpszCaption** <br/> |Janela restrita e sem janela restrita  <br/> |
|**lpszNewEntryTitle** <br/> |Modal  <br/> |
|**lpszDestWellsTitle**, **cDestFields**, **nDestFieldFocus**, **lppszDestTitles**e **lpulDestComps** <br/> |Modal  <br/> |
|**lpContRestriction** <br/> |Janela restrita e sem janela restrita  <br/> |
|**lpHierRestriction** <br/> |Janela restrita e sem janela restrita  <br/> |
   
A caixa de diálogo sem janela restrita é uma exibição somente leitura de entradas a partir de um ou mais contêineres do catálogo de endereços. A caixa de diálogo pode exibir todas as entradas a partir de contêineres selecionados ou ser limitado para apenas aqueles entradas e contêineres que correspondam aos critérios estabelecidos por uma restrição. A restrição de conteúdo apontada pela **lpContRestriction** pode limitar os tipos de entradas exibidas e a restrição de hierarquia apontada pela **lpHierRestriction** pode limitar os contêineres fornecendo as entradas. Para informar o chamador quando a caixa de diálogo é fechada, MAPI chama uma função que é fornecida pelo chamador que coincida com o protótipo [DISMISSMODELESS](dismissmodeless.md) . Outra função, que ele corresponda protótipo [ACCELERATEABSDI](accelerateabsdi.md) , é fornecida pelo MAPI e invocada pelo chamador no loop de mensagem do Windows para facilitar o trabalho de atalhos de teclado. A versão sem janela restrita da caixa de diálogo de endereço MAPI pode ser exibida quando clientes chamar [IAddrBook::Address](iaddrbook-address.md) ou quando os provedores de serviço chamarem [IMAPISupport::Address](imapisupport-address.md). 
  
A caixa de diálogo modal é uma exibição de leitura/gravação de entradas a partir de um ou mais contêineres. Seu conteúdo pode ser afetado da mesma maneira como a versão sem janela restrita por restrições definida no **lpContRestriction** and **lpHierRestriction** membros. Além da caixa de listagem exibindo entradas do contêiner, a caixa de diálogo modal pode conter entre um e três controles de caixa de texto para reter entradas selecionadas pelo usuário. Cada controle de edição é associado um determinado tipo de destinatário ou a propriedade **PR_RECIPIENT_TYPE** como MAPI_TO. A caixa de diálogo modal endereço pode ser exibida por qualquer um dos métodos **endereço** ou quando os clientes chamada [IAddrBook::Details](iaddrbook-details.md) e [IMAPISupport::Details](imapisupport-details.md)de chamada de provedores de serviços. 
  
Esta ilustração inclui dois controles de caixa de texto, porque o membro **cDestFields** da estrutura **ADRPARM** controlar a exibição dessa caixa de diálogo é definido como 2. O primeiro controle tem o foco inicial porque o membro **nDestFieldFocus** está definido como 0. 
  
O membro **lpszNewEntryTitle** aponta para o texto de um rótulo de botão que, quando ele for selecionado, faz com que uma caixa de diálogo adicionais a serem exibidos. Normalmente, conforme mostrado na ilustração da caixa de diálogo modal, o botão está rotulado **New** e a caixa de diálogo que aparece lista todos os tipos de endereços que podem ser criados por qualquer um dos provedores de catálogo de endereços no perfil. Clientes causam esta caixa de diálogo **Nova entrada** a ser exibido chamando [IAddrBook::NewEntry](iaddrbook-newentry.md) e passando zero para o parâmetro _cbEidNewEntryTpl_ e NULL para o parâmetro _lpEidNewEntryTpl_ quando o usuário seleciona o botão. As informações que estão incluídas nesta caixa de diálogo proveniente da tabela único de MAPI. 
  
Cada entrada nessa caixa de diálogo é associada um modelo para inserir os dados necessários para criar um endereço do tipo determinado. A maioria dos provedores de catálogo de endereços fornecer um modelo para cada tipo de entrada de endereço que possam criar. Quando um usuário faz uma seleção a partir dessa caixa de diálogo, o MAPI exibe o modelo correspondente.
  
Os quatro bits mais significativos do membro de **ulFlags** da estrutura **ADRPARM** contiverem um número de versão que identifica a versão da estrutura **ADRPARM** . A versão atual é 0 (zero) ou ADRPARM_HELP_CTX. A implementação atual do MAPI falhará para qualquer versão da estrutura diferente de zero. 
  
Versões futuras da estrutura podem ser completamente diferentes; eles podem não suportar a estrutura de versão de zero. As seguintes macros são fornecidas para extrair o número da versão do membro **ulFlags** em combinação com os sinalizadores definidos: 
  
- **GET_ADRPARM_VERSION** (_ulFlags_) 
- **SET_ADRPARM_VERSION** (_ulFlags_, _ ulVersion _) 
- **ADRPARM_HELP_CTX**
  
## <a name="see-also"></a>Confira também

- [ACCELERATEABSDI](accelerateabsdi.md)
- [DISMISSMODELESS](dismissmodeless.md)
- [IAddrBook::Address](iaddrbook-address.md)
- [IMAPISupport::Address](imapisupport-address.md)
- [SRestriction](srestriction.md)
- [Estruturas MAPI](mapi-structures.md)

