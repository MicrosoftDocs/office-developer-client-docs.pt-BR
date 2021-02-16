---
title: IMAPISupportDoCopyTo
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.DoCopyTo
api_type:
- COM
ms.assetid: 84019475-5176-4fc5-a3ee-871095077498
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 6f6c802f1d5ead1750c05fafc54533487fe3732a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32331805"
---
# <a name="imapisupportdocopyto"></a>IMAPISupport::DoCopyTo

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Copia ou move todas as propriedades de um objeto, exceto para propriedades especificamente excluídas, para outro objeto.
  
```cpp
HRESULT DoCopyTo(
  LPCIID lpSrcInterface,
  LPVOID lpSrcObj,
  ULONG ciidExclude,
  LPCIID rgiidExclude,
  LPSPropTagArray lpExcludeProps,
  ULONG_PTR ulUIParam,
  LPMAPIPROGRESS lpProgress,
  LPCIID lpDestInterface,
  LPVOID lpDestObj,
  ULONG ulFlags,
  LPSPropProblemArray FAR * lppProblems
);
```

## <a name="parameters"></a>Parâmetros

 _lpSrcInterface_
  
> [in] Um ponteiro para o IID (identificador de interface) que representa a interface a ser usada para acessar o objeto que tem as propriedades a serem copiadas ou movidas.
    
 _lpSrcObj_
  
> [in] Um ponteiro para o objeto que tem as propriedades a serem copiadas ou movidas.
    
 _ciidExclude_
  
> [in] A contagem de interfaces a excluir quando você copia ou move propriedades.
    
 _rgiidExclude_
  
> [in] Uma matriz de identificadores de interface que indica interfaces que não devem ser usadas quando você copia ou move informações complementares para o objeto de destino.
    
 _lpExcludeProps_
  
> [in] Um ponteiro para uma matriz de marcas de propriedade que identifica as marcas de propriedade que devem ser excluídas da operação de cópia ou movimentação. Passar NULL no  _parâmetro lpExcludeProps_ indica que todas as propriedades do objeto devem ser copiadas ou movidas. **DoCopyTo** retorna MAPI_E_INVALID_PARAMETER quando o membro **cValues** da estrutura [SPropTagArray](sproptagarray.md) apontado por  _lpExcludeProps_ é definido como 0. 
    
 _ulUIParam_
  
> [in] Um alça para a janela pai do indicador de progresso. 
    
 _lpProgress_
  
> [in] Um ponteiro para uma implementação do indicador de progresso. Se NULL for passado no  _parâmetro lpProgress,_ MAPI fornece a implementação de progresso. O _parâmetro lpProgress_ é ignorado, a menos que o sinalizador MAPI_DIALOG seja definido no _parâmetro ulFlags._ 
    
 _lpDestInterface_
  
> [in] Um ponteiro para o identificador da interface que representa a interface a ser usada para acessar o objeto a fim de receber as propriedades copiadas ou movidas.
    
 _lpDestObj_
  
> [in] Um ponteiro para o objeto para receber as propriedades copiadas ou movidas.
    
 _ulFlags_
  
> [in] Uma máscara de bits de sinalizadores que controla a operação de cópia ou movimentação. Os sinalizadores a seguir podem ser definidos:
    
MAPI_DIALOG 
  
> Exibe um indicador de progresso. 
    
MAPI_MOVE 
  
> **DoCopyTo** deve executar uma operação de movimentação em vez de uma operação de cópia. Quando esse sinalizador não está definido, **o DoCopyTo** executa uma operação de cópia. 
    
MAPI_NOREPLACE 
  
> As propriedades existentes no objeto de destino não devem ser substituídas. Quando esse sinalizador não estiver definido, **DoCopyTo** substituirá as propriedades existentes. 
    
 _lppProblems_
  
> [out] Na entrada, um ponteiro para um ponteiro para uma [estrutura SPropProblemArray;](spropproblemarray.md) caso contrário, NULL, que indica nenhuma necessidade de informações de erro. Se  _lppProblems_ for um ponteiro válido na entrada, **DoCopyTo** retornará informações detalhadas sobre erros ao copiar uma ou mais propriedades. 
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> As propriedades foram copiadas ou movidas com êxito.
    
MAPI_E_COLLISION 
  
> Uma propriedade a ser copiada ou movida já existe no objeto de destino e o MAPI_NOREPLACE sinalizador está definido. 
    
MAPI_E_FOLDER_CYCLE 
  
> O objeto de origem contém direta ou indiretamente o objeto de destino. Um trabalho significativo pode ter sido realizado antes dessa condição ser descoberta, portanto, os objetos de origem e destino podem ser parcialmente modificados. 
    
MAPI_E_INTERFACE_NOT_SUPPORTED 
  
> A interface identificada pelo parâmetro  _lpSrcInterface_ não é suportada pelo objeto apontado por  _lpSrcObj_ ou pela interface identificada pelo parâmetro  _lpDestInterface_ não é suportada pelo objeto apontado por  _lpDestObj_. 
    
MAPI_E_NO_ACCESS 
  
> Foi feita uma tentativa de acessar um objeto para o qual o chamador tem permissões insuficientes. Esse erro será retornado se o objeto de destino for o mesmo que o objeto de origem.
    
MAPI_E_INVALID_PARAMETER 
  
> O  _parâmetro lpSrcInterface_ é NULL. 
    
Os seguintes valores podem ser retornados na **estrutura SPropProblemArray,** mas não como valores de retorno para **DoCopyTo**. Esses erros se aplicam a uma única propriedade.
  
MAPI_E_BAD_CHARWIDTH 
  
> O sinalizador MAPI_UNICODE padrão foi definido e **DoCopyTo** não dá suporte a Unicode ou MAPI_UNICODE não foi definido e **DoCopyTo** dá suporte apenas a Unicode. 
    
MAPI_E_COMPUTED 
  
> A propriedade não pode ser modificada pelo chamador porque é uma propriedade somente leitura, calculada pelo proprietário do objeto de destino. Este erro não é grave; o chamador deve permitir que a operação de cópia continue.
    
MAPI_E_INVALID_TYPE 
  
> O tipo de propriedade é inválido.
    
MAPI_E_UNEXPECTED_TYPE 
  
> O tipo de propriedade não é o tipo esperado pelo chamador.
    
## <a name="remarks"></a>Comentários

O **método IMAPISupport::D oCopyTo** é implementado para objetos de suporte do provedor de armazenamento de mensagens. Os provedores de armazenamento de mensagens podem chamar **DoCopyTo** para implementar o método [IMAPIProp::CopyTo](imapiprop-copyto.md) para suas pastas e mensagens. 
  
Por padrão, **DoCopyTo** copia ou move todas as propriedades de um objeto para outro objeto. Quaisquer subobjetos no objeto de origem são automaticamente incluídos na operação e copiados ou movidos em sua totalidade. 
  
Se alguma das propriedades copiadas ou movidas já existir no objeto de destino, as propriedades existentes serão substituídas pelas novas propriedades, a menos que o sinalizador MAPI_NOREPLACE seja definido no parâmetro _ulFlags._ As informações existentes no objeto de destino que não são sobrescritas não são deixadas intocadas. 
  
## <a name="notes-to-callers"></a>Notas para chamadores

Para excluir propriedades da operação de movimentação ou cópia, inclua suas marcas de propriedade no _parâmetro lpExcludeProps._ Se você passar os resultados do uso da macro [PROP_TAG](prop_tag.md) para criar uma marca de propriedade de um identificador específico na matriz de marca de propriedade, todas as propriedades com esse identificador serão excluídas. Por exemplo, a seguinte entrada na matriz de marca de propriedade faz com que todas as propriedades com um identificador de 0x8002 sejam excluídas, independentemente do tipo: 
  
 `PROP_TAG(PT_LONG, 0x8002)`
  
Para evitar copiar o tempo de entrega de uma mensagem quando você copiar a mensagem para uma pasta diferente, especifique **PR_MESSAGE_DELIVERY_TIME** ([PidTagMessageDeliveryTime](pidtagmessagedeliverytime-canonical-property.md)) na matriz de exclusão da marca de propriedade. Para excluir a lista de destinatários de uma mensagem, adicione a propriedade **PR_MESSAGE_RECIPIENTS** ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md)) à matriz de exclusão. Para excluir os anexos de uma mensagem, adicione a **PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md)) à matriz.
  
Da mesma forma, para impedir a cópia ou movimentação da hierarquia ou do conteúdo de um contêiner de pasta ou de um contêiner de agendamento de endereços, inclua **PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md)) ou **PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md)) na matriz de exclusão de marca de propriedade.
  
Ignore MAPI_E_COMPUTED erros retornados na estrutura **SPropProblemArray** no _parâmetro lppProblems._ 
  
O identificador de interface que  _lpSrcInterface_ aponta é geralmente o mesmo que o identificador de interface que  _lpDestInterface_ aponta para. 
  
Se você passar um identificador de interface aceitável em  _lpDestInterface,_ mas um ponteiro inválido em  _lpDestObj_, os resultados serão imprevisíveis. Provavelmente, isso fará com que o provedor falhe. 
  
Por outro lado, se você estiver ciente das informações complementares que não devem ser copiadas ou movidas, adicione os identificadores de interface para as interfaces a serem excluídas na matriz passada no parâmetro _rgiidExclude._ Por exemplo, se você estiver copiando mensagens, mas não qualquer um de seus anexos de mensagem, passe IID_IMessage na matriz _rgiidExclude._ **DoCopyTo** ignora todas as interfaces listadas em  _rgiidExclude_ que ele não reconhece. 
  
Quando você usa o  _parâmetro rgiidExclude_ para excluir uma interface, ele também exclui todas as interfaces derivadas dessa interface. Por exemplo, excluir a interface [IMAPIContainer](imapicontainerimapiprop.md) faz com que pastas ou contêineres de agendamento de endereço sejam excluídos, dependendo do tipo de provedor. Não [exclua IMAPIProp](imapipropiunknown.md) [ou IUnknown](https://msdn.microsoft.com/library/33f1d79a-33fc-4ce5-a372-e08bda378332%28Office.15%29.aspx) porque muitas interfaces derivam delas. 
  
 **O DoCopyTo** relata erros globais que se aplicam à operação como um todo e erros individuais que se aplicam a propriedades individuais. Esses erros individuais são colocados em uma **estrutura SPropProblemArray.** Você pode suprimir o relatório de erros no nível da propriedade passando NULL, em vez de um ponteiro válido, para o parâmetro de estrutura da matriz do problema de propriedade. 
  
Se você quiser receber informações sobre erros, passe um ponteiro de estrutura **SPropProblemArray** válido no parâmetro _lppProblems._ Quando **DoCopyTo** retornar S_OK, verifique se há possíveis erros com propriedades individuais na estrutura. Quando **DoCopyTo** retorna um erro, nenhuma informação é retornada na **estrutura SPropProblemArray.** Em vez disso, chame [o método IMAPISupport::GetLastError](imapisupport-getlasterror.md) para recuperar informações de erro detalhadas. 
  
Se **DoCopyTo** retornar S_OK, livre a estrutura **SPropProblemArray** retornada chamando a [função MAPIFreeBuffer.](mapifreebuffer.md) 
  
Se ocorrer um erro global na chamada **DoCopyTo,** não use nem free a estrutura **SPropProblemArray.** Os provedores devem ignorar  _o membro ulIndex_ em **estruturas SPropProblemArray** retornadas por **DoCopyTo**.
  
## <a name="see-also"></a>Confira também



[IMAPIProp::CopyTo](imapiprop-copyto.md)
  
[IMAPISupport::CopyFolder](imapisupport-copyfolder.md)
  
[IMAPISupport::CopyMessages](imapisupport-copymessages.md)
  
[IMAPISupport::GetLastError](imapisupport-getlasterror.md)
  
[Propriedade canônica PidTagContainerContents](pidtagcontainercontents-canonical-property.md)
  
[Propriedade canônica PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md)
  
[Propriedade canônica PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md)
  
[Propriedade canônica PidTagMessageDeliveryTime](pidtagmessagedeliverytime-canonical-property.md)
  
[Propriedade canônica PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md)
  
[SPropProblemArray](spropproblemarray.md)
  
[SPropTagArray](sproptagarray.md)
  
[IMAPISupport: IUnknown](imapisupportiunknown.md)

