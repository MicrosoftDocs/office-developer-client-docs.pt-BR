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
ms.openlocfilehash: 9663a25a50d914f47cff48124898d16318bbbc43
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33425894"
---
# <a name="adrparm"></a>ADRPARM

**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Descreve a exibição e o comportamento da caixa de diálogo endereço comum. 
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |Mapidefs. h  <br/> |
   
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
  
> Contagem de bytes no identificador de entrada apontado por **lpABContEntryID**.
    
**lpABContEntryID**
  
> Ponteiro para o identificador de entrada do contêiner que fornece a lista inicial de endereços de destinatário que são exibidos na caixa de diálogo de endereço.
    
**ulFlags**
  
> Bitmask de sinalizadores associados a várias opções da caixa de diálogo de endereço. Os seguintes sinalizadores podem ser definidos:
    
AB_RESOLVE
  
> Habilitar todos os nomes a serem resolvidos depois que a caixa de diálogo de endereço for fechada. Se houver entradas ambíguas que resultem do processo de resolução de nomes, uma caixa de diálogo será exibida para solicitar ajuda ao usuário para solucioná-los. A definição desse sinalizador garante que todos os nomes retornados por [IAddrBook:: address](iaddrbook-address.md) sejam resolvidos. 
    
AB_SELECTONLY
  
> Desabilitar a criação de endereços únicos para uma lista de destinatários. Este sinalizador é usado apenas se a caixa de diálogo for modal, conforme indicado pelo sinalizador DIALOG_MODAL que está sendo definido.
    
ADDRESS_ONE
  
> O usuário pode selecionar exatamente um destinatário em vez de vários destinatários de uma lista. Este sinalizador é válido somente quando o **cDestFields** é zero e a caixa de diálogo é modal, conforme indicado pelo sinalizador DIALOG_MODAL que está sendo definido. 
    
DIALOG_MODAL
  
> Faz com que a versão modal da caixa de diálogo de endereço comum seja exibida. Este sinalizador ou DIALOG_SDI deve ser definido; Eles não podem ser definidos. 
    
DIALOG_OPTIONS
  
> Faz com que o botão **Opções de envio** seja exibido na caixa de diálogo. Este sinalizador é usado apenas se a caixa de diálogo for modal, conforme indicado pelo sinalizador DIALOG_MODAL que está sendo definido. 
    
DIALOG_SDI
  
> Faz com que a versão sem janela restrita da caixa de diálogo de endereço comum seja exibida. Este sinalizador ou DIALOG_MODAL deve ser definido; Eles não podem ser definidos. O sinalizador DIALOG_SDI é ignorado para clientes que não são do Outlook e a versão modal da caixa de diálogo será exibida. Consequentemente, um ponteiro para um identificador não deve ser esperado no parâmetro _lpulUIParam_ de [IAddrBook:: address](iaddrbook-address.md).
    
**lpReserved**
  
> Reservado, deve ser zero.
    
**ulHelpContext**
  
> Especifica o contexto dentro da **ajuda** que será mostrado primeiro quando o usuário clicar no botão ajuda na caixa de diálogo endereço. 
    
**lpszHelpFileName**
  
> Ponteiro para o nome de um arquivo de ajuda que será associado à caixa de diálogo de endereço. O membro **lpszHelpFileName** é usado em conjunto com o **ulHelpContext** para chamar a função **WinHelp** do Windows. 
    
**lpfnABSDI**
  
> Ponteiro para uma função MAPI com base no protótipo [ACCELERATEABSDI](accelerateabsdi.md) ou nulo. Este membro se aplica à versão sem janela restrita da caixa de diálogo apenas, conforme indicado pelo sinalizador DIALOG_SDI que está sendo definido. Os clientes que criam uma estrutura **ADRPARM** para passar para o [IAddrBook:: o endereço](iaddrbook-address.md) deve sempre definir o membro **lpfnABSDI** como nulo. Se o sinalizador DIALOG_SDI estiver definido, o MAPI irá defini-lo como uma função válida antes de retornar. Os clientes chamam essa função no loop de mensagens para garantir que os aceleradores da caixa de diálogo do catálogo de endereços funcionem. Quando a caixa de diálogo é ignorada e MAPI chama a função indicada pelo membro **lpfnDismiss** , os clientes devem desenganchar a função **ACCELERATEABSDI** de seu loop de mensagem. 
    
**lpfnDismiss**
  
> Ponteiro para uma função com base no protótipo [DISMISSMODELESS](dismissmodeless.md) ou nulo. Este membro só se aplica à versão sem janela restrita da caixa de diálogo, conforme indicado pelo sinalizador DIALOG_SDI que está sendo definido. MAPI chama a função **DISMISSMODELESS** quando o usuário ignora a caixa de diálogo de endereço sem restrições, informando um cliente chamando **IAddrBook:: address** que a caixa de diálogo não está mais ativa. 
    
**lpvDismissContext**
  
> Ponteiro para informações de contexto a serem passadas para a função **DISMISSMODELESS** indicada pelo membro **lpfnDismiss** . Este membro se aplica apenas à versão sem janela restrita da caixa de diálogo, conforme indicado pelo sinalizador DIALOG_SDI que está sendo definido. 
    
**lpszCaption**
  
> Ponteiro para o texto a ser usado como o título da caixa de diálogo endereço comum.
    
**lpszNewEntryTitle**
  
> Ponteiro para o texto a ser usado como o rótulo do botão que invoca a caixa de diálogo **nova entrada** ou outra caixa de diálogo. 
    
**lpszDestWellsTitle**
  
> Ponteiro para o texto a ser usado como um título para os controles de caixa de texto do destinatário que podem aparecer na versão modal da caixa de diálogo endereço comum. Este membro não é usado para caixas de diálogo sem restrições. 
    
**cDestFields**
  
> Contagem de controles de caixa de texto do destinatário na versão modal da caixa de diálogo endereço ou zero se a caixa de diálogo for sem restrições. A caixa de diálogo endereço é aberta para navegação somente quando as seguintes condições forem verdadeiras: 
    
  - O membro **cDestFields** está definido como zero. 
    
  - O sinalizador DIALOG_BOX está definido.
    
  - O sinalizador ADDRESS_ONE não está definido.
    
  A definição de **cDestFields** como 0xFFFFFFFF implica que o MAPI deve criar o número padrão de controles de caixa de texto do destinatário. Nesse caso, os membros **lppszDestTitles** e **LPULDESTCOMPS** devem ser nulos. 
    
**nDestFieldFocus**
  
> Indica o controle de caixa de texto específico que deverá ter o foco inicial quando a versão modal da caixa de diálogo for exibida. Esse valor deve estar entre 0 e o valor de **cDestFields** menos 1. 
    
**lppszDestTitles**
  
> Ponteiro para uma matriz de rótulos de botões associados a cada um dos controles de caixa de texto que são exibidos na versão modal da caixa de diálogo de endereço. O valor do membro **cDestFields** indica o número de rótulos incluídos na matriz. Se o membro **lppszDestTitles** for nulo, o método **Address** usará títulos padrão. 
    
**lpulDestComps**
  
> Ponteiro para uma matriz de valores de tipo de destinatário, como MAPI_TO, MAPI_CC e MAPI_BCC, que é associado a cada controle de caixa de texto. O valor do membro **CDestFields** indica o número de tipos de destinatários incluídos na matriz. Os valores apontados por **lpulDestComps** podem ser usados para definir a propriedade **PR_RECIPIENT_TYPE** ([PidTagRecipientType](pidtagrecipienttype-canonical-property.md)) de cada destinatário. Se o membro **lpulDestComps** for nulo, o método **Address** usará tipos de destinatário padrão. 
    
**lpContRestriction**
  
> Ponteiro para uma estrutura [SRestriction](srestriction.md) que limita o tipo de entradas de endereço que podem ser exibidas na caixa de diálogo. 
    
**lpHierRestriction**
  
> Ponteiro para uma estrutura **SRestriction** que limita os contêineres do catálogo de endereços que podem fornecer entradas de endereço a serem exibidas na caixa de diálogo. 
    
## <a name="remarks"></a>Comentários

As estruturas **ADRPARM** são usadas por clientes e provedores de serviço para controlar a aparência e o comportamento das caixas de diálogo de endereço comum MAPI. Há duas variedades da caixa de diálogo de endereço: sem-modo e modal. Alguns membros da estrutura **ADRPARM** aplicam-se às duas versões da caixa de diálogo, mas algumas só se aplicam a uma das duas versões. A tabela a seguir relaciona os membros de uma estrutura **ADRPARM** ao uso com as caixas de diálogo de endereço comum. 
  
|Membro ADRPARM|Tipo de caixa de diálogo|
|:-----|:-----|
|**cbABContEntryID** e **lpABContEntryID** <br/> |Modal e sem janela restrita  <br/> |
|**ulFlags** <br/> |Modal e sem janela restrita  <br/> |
|**lpReserved** <br/> |Modal e sem janela restrita  <br/> |
|**ulHelpContext** e **lpszHelpFileName** <br/> |Modal e sem janela restrita  <br/> |
|**lpfnABSDI** <br/> |Sem janela restrita  <br/> |
|**lpfnDismiss** e **lpvDismissContext** <br/> |Sem janela restrita  <br/> |
|**lpszCaption** <br/> |Modal e sem janela restrita  <br/> |
|**lpszNewEntryTitle** <br/> |Modal  <br/> |
|**lpszDestWellsTitle**, **cDestFields**, **nDestFieldFocus**, **lppszDestTitles**e **lpulDestComps** <br/> |Modal  <br/> |
|**lpContRestriction** <br/> |Modal e sem janela restrita  <br/> |
|**lpHierRestriction** <br/> |Modal e sem janela restrita  <br/> |
   
A caixa de diálogo sem-modo é uma exibição somente leitura das entradas de um ou mais contêineres do catálogo de endereços. A caixa de diálogo pode exibir todas as entradas dos contêineres selecionados ou ser limitada apenas às entradas e aos contêineres que correspondam aos critérios estabelecidos por uma restrição. A restrição de conteúdo indicada por **lpContRestriction** pode limitar os tipos de entradas exibidas e a restrição de hierarquia indicada por **lpHierRestriction** pode limitar os contêineres que fornecem as entradas. Para informar o chamador quando a caixa de diálogo é ignorada, o MAPI invoca uma função que é fornecida pelo chamador que corresponde ao protótipo [DISMISSMODELESS](dismissmodeless.md) . Outra função, que corresponde ao protótipo [ACCELERATEABSDI](accelerateabsdi.md) , é fornecida por MAPI e invocada pelo chamador no loop de mensagem do Windows para facilitar o trabalho de atalhos de teclado. A versão sem restrições da caixa de diálogo de endereço MAPI pode ser exibida quando os clientes chamam [IAddrBook:: address](iaddrbook-address.md) ou quando os provedores de serviço chamam [IMAPISupport:: address](imapisupport-address.md). 
  
A caixa de diálogo modal é uma exibição de leitura/gravação de entradas de um ou mais contêineres. Seu conteúdo pode ser afetado da mesma maneira que a versão sem janela restrita por restrições definidas nos membros **lpContRestriction** e **lpHierRestriction** . Além da caixa de listagem exibindo entradas de contêiner, a caixa de diálogo modal pode conter entre um e três controles de caixa de texto para conter entradas selecionadas pelo usuário. Cada controle de edição é associado a um tipo de destinatário específico ou a propriedade **PR_RECIPIENT_TYPE** , como MAPI_TO. A caixa de diálogo Endereço modal pode ser exibida por qualquer um dos métodos **Address** ou quando os clientes chamam [IAddrBook::D etails](iaddrbook-details.md) e provedores de serviço chamam [IMAPISupport::D etails](imapisupport-details.md). 
  
Esta ilustração inclui dois controles de caixa de texto porque o membro **cDestFields** da estrutura **ADRPARM** que controla a exibição dessa caixa de diálogo é definido como 2. O primeiro controle tem o foco inicial porque o membro **nDestFieldFocus** está definido como 0. 
  
O membro **lpszNewEntryTitle** aponta para o texto de um rótulo de botão que, quando é selecionado, faz com que uma caixa de diálogo adicional seja exibida. Normalmente, como é mostrado na ilustração da caixa de diálogo modal, o botão é rotulado como **novo** e a caixa de diálogo exibida lista todos os tipos de endereços que podem ser criados por qualquer um dos provedores de catálogo de endereços no perfil. Os clientes fazem com que essa nova caixa de diálogo de **entrada** seja exibida chamando [IAddrBook:: NewEntry](iaddrbook-newentry.md) e passando zero para o parâmetro _cbEidNewEntryTpl_ e nulo para o parâmetro _lpEidNewEntryTpl_ quando o usuário seleciona o botão. As informações incluídas nessa caixa de diálogo vêm da tabela de one-off MAPI. 
  
Cada entrada nessa caixa de diálogo é associada a um modelo para inserir os dados necessários para criar um endereço do tipo específico. A maioria dos provedores de catálogos de endereços fornecem um modelo para cada tipo de entrada de endereço que eles podem criar. Quando um usuário faz uma seleção nessa caixa de diálogo, MAPI exibe o modelo correspondente.
  
Os quatro bits mais significativos do membro **parâmetroulflags** da estrutura **ADRPARM** contêm um número de versão que identifica a versão da estrutura **ADRPARM** . A versão atual é 0 (zero) ou ADRPARM_HELP_CTX. A implementação atual de MAPI irá falhar para qualquer versão da estrutura diferente de zero. 
  
Versões futuras da estrutura podem ser completamente diferentes; Eles podem não oferecer suporte à estrutura de versão zero. As macros a seguir são fornecidas para extrair o número de versão do membro **parâmetroulflags** e para combiná-lo com os sinalizadores definidos: 
  
- **GET_ADRPARM_VERSION** (_parâmetroulflags_) 
- **SET_ADRPARM_VERSION** (_parâmetroulflags_, _ ulVersion _) 
- **ADRPARM_HELP_CTX**
  
## <a name="see-also"></a>Confira também

- [ACCELERATEABSDI](accelerateabsdi.md)
- [DISMISSMODELESS](dismissmodeless.md)
- [IAddrBook::Address](iaddrbook-address.md)
- [IMAPISupport::Address](imapisupport-address.md)
- [SRestriction](srestriction.md)
- [Estruturas MAPI](mapi-structures.md)

