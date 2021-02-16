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
  
Descreve a exibição e o comportamento da caixa de diálogo de endereço comum. 
  
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
  
> Contagem de bytes no identificador de entrada apontado por **lpABContEntryID**.
    
**lpABContEntryID**
  
> Ponteiro para o identificador de entrada do contêiner que fornece a lista inicial de endereços de destinatários que são exibidos na caixa de diálogo de endereço.
    
**ulFlags**
  
> Máscara de bits de sinalizadores associados a várias opções de caixa de diálogo de endereço. Os sinalizadores a seguir podem ser definidos:
    
AB_RESOLVE
  
> Habilita todos os nomes a serem resolvidos depois que a caixa de diálogo de endereço é fechada. Se houver entradas ambíguas resultantes do processo de resolução de nomes, uma caixa de diálogo aparecerá solicitando ao usuário ajuda para resolvê-las. Definir esse sinalizador garante que todos os nomes retornados por [IAddrBook::Address](iaddrbook-address.md) sejam resolvidos. 
    
AB_SELECTONLY
  
> Desabilite a criação de endereços one-off para uma lista de destinatários. Esse sinalizador é usado somente se a caixa de diálogo for modal, conforme indicado pelo sinalizador DIALOG_MODAL está sendo definido.
    
ADDRESS_ONE
  
> O usuário pode selecionar exatamente um destinatário em vez de vários destinatários de uma lista. Esse sinalizador só é válido quando **cDestFields** é zero e a caixa de diálogo é modal, conforme indicado pelo sinalizador DIALOG_MODAL está sendo definido. 
    
DIALOG_MODAL
  
> Faz com que a versão modal da caixa de diálogo de endereço comum seja exibida. Esse sinalizador ou DIALOG_SDI deve ser definido; eles não podem ser definidos. 
    
DIALOG_OPTIONS
  
> Faz com **que o** botão Opções de Envio seja exibido na caixa de diálogo. Esse sinalizador é usado somente se a caixa de diálogo for modal, conforme indicado pelo sinalizador DIALOG_MODAL está sendo definido. 
    
DIALOG_SDI
  
> Faz com que a versão sem modo da caixa de diálogo de endereço comum seja exibida. Esse sinalizador ou DIALOG_MODAL deve ser definido; eles não podem ser definidos. O DIALOG_SDI sinalizador é ignorado para clientes que não são do Outlook e a versão modal da caixa de diálogo será exibida. Consequentemente, um ponteiro para um indicador não deve ser esperado no parâmetro  _lpulUIParam_ de [IAddrBook::Address](iaddrbook-address.md).
    
**lpReserved**
  
> Reservado, deve ser zero.
    
**ulHelpContext**
  
> Especifica o contexto na **Ajuda** que será exibido primeiro quando o usuário clicar no botão Ajuda na caixa de diálogo de endereço. 
    
**lpszHelpFileName**
  
> Ponteiro para o nome de um arquivo de Ajuda que será associado à caixa de diálogo de endereço. O **membro lpszHelpFileName** é usado junto com **ulHelpContext** para chamar a função **WinHelp do** Windows. 
    
**lpfnABSDI**
  
> Ponteiro para uma função MAPI com base no protótipo [ACCELERATEABSDI](accelerateabsdi.md) ou NULL. Esse membro se aplica somente à versão sem modo da caixa de diálogo, conforme indicado pelo sinalizador DIALOG_SDI está sendo definido. Os clientes que estão criando uma estrutura **ADRPARM** para passar para [IAddrBook::Address](iaddrbook-address.md) devem sempre definir o membro **lpfnABSDI** como NULL. Se o DIALOG_SDI sinalizador estiver definido, o MAPI o definirá como uma função válida antes de retornar. Os clientes chamam essa função no loop de mensagens para garantir que os aceleradores na caixa de diálogo do livro de endereços funcionem. Quando a caixa de diálogo é descartada e MAPI chama a função apontada pelo membro **lpfnDismiss,** os clientes devem desaconsinchar a função **ACCELERATEABSDI** de seu loop de mensagem. 
    
**lpfnDismiss**
  
> Ponteiro para uma função baseada no protótipo [DISMISSMODELESS](dismissmodeless.md) ou NULL. Esse membro só se aplica à versão sem modo da caixa de diálogo, conforme indicado pelo sinalizador DIALOG_SDI está sendo definido. MAPI calls the **DISMISSMODELESS function** when the user dismisses the modeless address dialog box, informing a client calling **IAddrBook::Address** that the dialog box is no longer active. 
    
**lpvDismissContext**
  
> Ponteiro para informações de contexto a serem passadas para a **função DISMISSMODELESS** apontada pelo **membro lpfnDismiss.** Este membro aplica-se somente à versão sem modo da caixa de diálogo, conforme indicado pelo sinalizador DIALOG_SDI está sendo definido. 
    
**lpszCaption**
  
> Ponteiro para texto a ser usado como o título da caixa de diálogo de endereço comum.
    
**lpszNewEntryTitle**
  
> Ponteiro para texto a ser usado como o rótulo  do botão para o botão que invoca a caixa de diálogo Nova Entrada ou outra caixa de diálogo. 
    
**lpszDestWellsTitle**
  
> Ponteiro para texto a ser usado como um título para os controles de caixa de texto do destinatário que podem aparecer na versão modal da caixa de diálogo de endereço comum. Este membro não é usado para caixas de diálogo sem modo. 
    
**cDestFields**
  
> Contagem de controles de caixa de texto do destinatário na versão modal da caixa de diálogo de endereço ou zero se a caixa de diálogo não tiver nenhuma. A caixa de diálogo de endereço está aberta para navegação somente quando as seguintes condições são verdadeiras: 
    
  - O **membro cDestFields** é definido como zero. 
    
  - O DIALOG_BOX sinalizador está definido.
    
  - O ADDRESS_ONE sinalizador não está definido.
    
  Definir **cDestFields** como 0XFFFFFFFF indica que MAPI deve criar o número padrão de controles de caixa de texto do destinatário. Nesse caso, os **membros lppszDestTitles** e **lpulDestComps** devem ser NULL. 
    
**nDestFieldFocus**
  
> Indica o controle de caixa de texto específico que deve ter o foco inicial quando a versão modal da caixa de diálogo for exibida. Esse valor deve estar entre 0 e o valor de **cDestFields** menos 1. 
    
**lppszDestTitles**
  
> Ponteiro para uma matriz de rótulos para botões associados a cada um dos controles de caixa de texto que são exibidos na versão modal da caixa de diálogo de endereço. O valor do **membro cDestFields** indica o número de rótulos incluídos na matriz. Se o **membro lppszDestTitles** for NULL, o método **Address** usará títulos padrão. 
    
**lpulDestComps**
  
> Ponteiro para uma matriz de valores de tipo de destinatário, como MAPI_TO, MAPI_CC e MAPI_BCC, que está associada a cada controle de caixa de texto. O valor do **membro CDestFields** indica o número de tipos de destinatários incluídos na matriz. Os valores apontados por **lpulDestComps** podem ser usados para definir a propriedade **PR_RECIPIENT_TYPE** ([PidTagRecipientType](pidtagrecipienttype-canonical-property.md)) de cada destinatário. Se o **membro lpulDestComps** for NULL, o método **Address** usará tipos de destinatário padrão. 
    
**lpContRestriction**
  
> Ponteiro para uma [estrutura SRestriction](srestriction.md) que limita o tipo de entradas de endereço que podem ser exibidas na caixa de diálogo. 
    
**lpHierRestriction**
  
> Ponteiro para uma **estrutura SRestriction** que limita os contêineres do livro de endereços que podem fornecer entradas de endereço a serem exibidas na caixa de diálogo. 
    
## <a name="remarks"></a>Comentários

**As estruturas ADRPARM** são usadas por clientes e provedores de serviços para controlar a aparência e o comportamento das caixas de diálogo de endereço comuns MAPI. Há duas variedades de caixa de diálogo de endereço: sem modo e modal. Alguns dos membros na estrutura **ADRPARM** se aplicam às duas versões da caixa de diálogo, mas alguns se aplicam apenas a uma das duas versões. A tabela a seguir relaciona os membros de uma estrutura **ADRPARM** ao seu uso com as caixas de diálogo de endereço comuns. 
  
|Membro ADRPARM|Tipo de caixa de diálogo|
|:-----|:-----|
|**cbABContEntryID** e **lpABContEntryID** <br/> |Modal e sem modo  <br/> |
|**ulFlags** <br/> |Modal e sem modo  <br/> |
|**lpReserved** <br/> |Modal e sem modo  <br/> |
|**ulHelpContext** e **lpszHelpFileName** <br/> |Modal e sem modo  <br/> |
|**lpfnABSDI** <br/> |Sem modo  <br/> |
|**lpfnDismiss** e **lpvDismissContext** <br/> |Sem modo  <br/> |
|**lpszCaption** <br/> |Modal e sem modo  <br/> |
|**lpszNewEntryTitle** <br/> |Modal  <br/> |
|**lpszDestWellsTitle**, **cDestFields**, **nDestFieldFocus**, **lppszDestTitles** e **lpulDestComps** <br/> |Modal  <br/> |
|**lpContRestriction** <br/> |Modal e sem modo  <br/> |
|**lpHierRestriction** <br/> |Modal e sem modo  <br/> |
   
A caixa de diálogo sem modo é uma exibição somente leitura de entradas de um ou mais contêineres de livro de endereços. A caixa de diálogo pode exibir todas as entradas dos contêineres selecionados ou ser limitada apenas às entradas e contêineres que corresponderem aos critérios estabelecidos por uma restrição. A restrição de conteúdo apontada por **lpContRestriction** pode limitar os tipos de entradas exibidas, e a restrição de hierarquia apontada por **lpHierRestriction** pode limitar os contêineres que fornecerem as entradas. Para informar ao chamador quando a caixa de diálogo é descartada, o MAPI invoca uma função fornecida pelo chamador que corresponde ao protótipo [DISMISSMODELESS.](dismissmodeless.md) Outra função, que corresponde ao protótipo [ACCELERATEABSDI,](accelerateabsdi.md) é fornecida por MAPI e invocada pelo chamador no loop de mensagens do Windows para facilitar o trabalho de atalhos de teclado. A versão sem modo da caixa de diálogo endereço MAPI pode ser exibida quando os clientes chamam [IAddrBook::Address](iaddrbook-address.md) ou quando os provedores de serviços chamam [IMAPISupport::Address](imapisupport-address.md). 
  
A caixa de diálogo modal é uma exibição de leitura/gravação de entradas de um ou mais contêineres. Seu conteúdo pode ser afetado da mesma maneira que a versão sem restrições definida nos membros **lpContRestriction** e **lpHierRestriction.** Além da caixa de listagem exibindo entradas de contêiner, a caixa de diálogo modal pode conter entre um e três controles de caixa de texto para manter entradas selecionadas pelo usuário. Cada controle de edição é associado a um determinado tipo de destinatário **ou** PR_RECIPIENT_TYPE propriedade, como MAPI_TO. A caixa de diálogo endereço modal pode ser exibida por qualquer um dos métodos **address** ou quando os clientes chamam [IAddrBook::D etails](iaddrbook-details.md) and service providers call [IMAPISupport::D etails](imapisupport-details.md). 
  
Esta ilustração inclui dois controles de caixa de texto porque o membro **cDestFields** da estrutura **ADRPARM** que controla a exibição dessa caixa de diálogo é definido como 2. O primeiro controle tem foco inicial porque o **membro nDestFieldFocus** está definido como 0. 
  
O **membro lpszNewEntryTitle** aponta para o texto de um rótulo de botão que, quando selecionado, faz com que uma caixa de diálogo adicional seja exibida. Normalmente, como é mostrado na ilustração da caixa de diálogo  modal, o botão é rotulado como Novo e a caixa de diálogo que aparece lista todos os tipos de endereços que podem ser criados por qualquer um dos provedores de agenda do perfil. Os clientes  podem exibir essa caixa de diálogo Nova Entrada chamando [IAddrBook::NewEntry](iaddrbook-newentry.md) e passando zero para o parâmetro _cbEidNewEntryTpl_ e NULL para o parâmetro _lpEidNewEntryTpl_ quando o usuário seleciona o botão. As informações incluídas nesta caixa de diálogo vêm da tabela única MAPI. 
  
Cada entrada nessa caixa de diálogo é associada a um modelo para inserir os dados necessários para criar um endereço do tipo específico. A maioria dos provedores de livro de endereços fornece um modelo para cada tipo de entrada de endereço que eles podem criar. Quando um usuário faz uma seleção a partir dessa caixa de diálogo, MAPI exibe o modelo correspondente.
  
Os quatro bits mais significativos do membro **ulFlags** da estrutura **ADRPARM** contêm um número de versão que identifica a versão da estrutura **ADRPARM.** A versão atual é 0 (zero) ou ADRPARM_HELP_CTX. A implementação atual do MAPI falhará para qualquer versão da estrutura diferente de zero. 
  
Versões futuras da estrutura podem ser completamente diferentes; eles podem não dar suporte à estrutura de versão zero. As macros a seguir são fornecidas para extrair o número de versão do membro **ulFlags** e combiná-lo com os sinalizadores definidos: 
  
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

