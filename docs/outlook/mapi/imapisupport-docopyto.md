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
  
Copia ou move todas as propriedades de um objeto, exceto as propriedades especificamente excluídas, para outro objeto.
  
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
  
> no Um ponteiro para o identificador de interface (IID) que representa a interface a ser usada para acessar o objeto que tem as propriedades a serem copiadas ou movidas.
    
 _lpSrcObj_
  
> no Um ponteiro para o objeto que tem as propriedades a serem copiadas ou movidas.
    
 _ciidExclude_
  
> no A contagem de interfaces a serem excluídas quando você copia ou move Propriedades.
    
 _rgiidExclude_
  
> no Uma matriz de identificadores de interface que indica interfaces que não devem ser usadas quando você copia ou move informações complementares para o objeto de destino.
    
 _lpExcludeProps_
  
> no Um ponteiro para uma matriz de marca de propriedade que identifica as marcas de propriedade que devem ser excluídas da operação de cópia ou movimentação. Passar NULL no parâmetro _lpExcludeProps_ indica que todas as propriedades do objeto devem ser copiadas ou movidas. **** Docopyto retorna MAPI_E_INVALID_PARAMETER quando o membro **CValues** da estrutura [SPropTagArray](sproptagarray.md) apontada por _lpExcludeProps_ é definida como 0. 
    
 _ulUIParam_
  
> no Uma alça para a janela pai do indicador de progresso. 
    
 _lpProgress_
  
> no Um ponteiro para uma implementação de indicador de progresso. Se NULL for passado no parâmetro _lpProgress_ , MAPI fornecerá a implementação de progresso. O parâmetro _lpProgress_ é ignorado, a menos que o sinalizador MAPI_DIALOG esteja definido no parâmetro _parâmetroulflags_ . 
    
 _lpDestInterface_
  
> no Um ponteiro para o identificador de interface que representa a interface a ser usada para acessar o objeto para receber as propriedades copiadas ou movidas.
    
 _lpDestObj_
  
> no Um ponteiro para o objeto para receber as propriedades copiadas ou movidas.
    
 _ulFlags_
  
> no Uma bitmask de sinalizadores que controlam a operação de cópia ou movimentação. Os seguintes sinalizadores podem ser definidos:
    
MAPI_DIALOG 
  
> Exibe um indicador de progresso. 
    
MAPI_MOVE 
  
> **** Docopyto deve executar uma operação de movimentação em vez de uma operação de cópia. Quando esse sinalizador não é definido, **** docopyto realiza uma operação de cópia. 
    
MAPI_NOREPLACE 
  
> As propriedades existentes no objeto de destino não devem ser substituídas. Quando esse sinalizador não é definido, **** docopyto substitui as propriedades existentes. 
    
 _lppProblems_
  
> bota Na entrada, um ponteiro para um ponteiro para uma estrutura [SPropProblemArray](spropproblemarray.md) ; caso contrário, NULL, que não indica nenhuma necessidade de informações de erro. Se _lppProblems_ for um ponteiro válido na entrada, **** docopyto retornará informações detalhadas sobre erros ao copiar uma ou mais propriedades. 
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> As propriedades foram copiadas ou movidas com êxito.
    
MAPI_E_COLLISION 
  
> Uma propriedade a ser copiada ou movida já existe no objeto de destino e o sinalizador MAPI_NOREPLACE está definido. 
    
MAPI_E_FOLDER_CYCLE 
  
> O objeto de origem direta ou indiretamente contém o objeto de destino. Um trabalho significativo pode ter sido realizado antes da descoberta dessa condição, portanto, os objetos de origem e de destino podem ser parcialmente modificados. 
    
MAPI_E_INTERFACE_NOT_SUPPORTED 
  
> A interface identificada pelo parâmetro _lpSrcInterface_ não é suportada pelo objeto apontado por _lpSrcObj_ou a interface identificada pelo parâmetro _lpDestInterface_ não é suportada pelo objeto apontado por _lpDestObj _. 
    
MAPI_E_NO_ACCESS 
  
> Foi feita uma tentativa de acessar um objeto para o qual o chamador tem permissões insuficientes. Esse erro será retornado se o objeto de destino for o mesmo que o objeto de origem.
    
MAPI_E_INVALID_PARAMETER 
  
> O parâmetro _lpSrcInterface_ é NULL. 
    
Os valores a seguir podem ser retornados na estrutura **SPropProblemArray** , mas não como valores de retorno **** para docopyto. Esses erros se aplicam a uma única propriedade.
  
MAPI_E_BAD_CHARWIDTH 
  
> O sinalizador MAPI_UNICODE foi definido e doCopyto não tem suporte para Unicode, ou MAPI_UNICODE não foi definido e **Docopyto** suporta apenas Unicode. **** 
    
MAPI_E_COMPUTED 
  
> A propriedade não pode ser modificada pelo chamador porque é uma propriedade somente leitura, calculada pelo proprietário do objeto de destino. Esse erro não é grave; o chamador deve permitir que a operação de cópia continue.
    
MAPI_E_INVALID_TYPE 
  
> O tipo de propriedade é inválido.
    
MAPI_E_UNEXPECTED_TYPE 
  
> O tipo de propriedade não é o tipo esperado pelo chamador.
    
## <a name="remarks"></a>Comentários

O método **IMAPISupport::D ocopyto** é implementado para objetos de suporte do provedor de repositório de mensagens. Os provedores de repositórios **** de mensagens podem chamar docopyto para implementar o método [IMAPIProp:: CopyTo](imapiprop-copyto.md) para suas pastas e mensagens. 
  
Por padrão, **** docopyto copia ou move todas as propriedades de um objeto para outro objeto. Todos os subobjetos no objeto de origem são automaticamente incluídos na operação e copiados ou movidos completamente. 
  
Se qualquer uma das propriedades copiadas ou movidas já existir no objeto de destino, as propriedades existentes serão sobrescritas pelas novas propriedades, a menos que o sinalizador MAPI_NOREPLACE seja definido no parâmetro _parâmetroulflags_ . As informações existentes no objeto de destino que não estão sobrescritas são deixadas inalteradas. 
  
## <a name="notes-to-callers"></a>Notas para chamadores

Para excluir propriedades da operação de cópia ou movimentação, inclua suas marcas de propriedade no parâmetro _lpExcludeProps_ . Se você passar os resultados do uso da macro [PROP_TAG](prop_tag.md) para criar uma marca de propriedade a partir de um identificador específico na matriz de marca de propriedade, todas as propriedades com esse identificador serão excluídas. Por exemplo, a seguinte entrada na matriz de marca de propriedade faz com que todas as propriedades com um identificador de 0x8002 sejam excluídas, independentemente do tipo: 
  
 `PROP_TAG(PT_LONG, 0x8002)`
  
Para evitar a cópia do tempo de entrega de uma mensagem quando você copia a mensagem para uma pasta diferente, especifique **PR_MESSAGE_DELIVERY_TIME** ([PidTagMessageDeliveryTime](pidtagmessagedeliverytime-canonical-property.md)) na marca de propriedade Exclude array. Para excluir a lista de destinatários de uma mensagem, adicione a propriedade **PR_MESSAGE_RECIPIENTS** ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md)) à matriz Exclude. Para excluir os anexos de uma mensagem, adicione a propriedade **PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md)) à matriz.
  
Da mesma forma, para impedir a cópia ou a movimentação de uma pasta ou hierarquia de um contêiner de catálogo de endereços ou uma tabela de conteúdo, inclua **PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md)) ou **PR_CONTAINER_CONTENTS** ([ PidTagContainerContents](pidtagcontainercontents-canonical-property.md)) na marca Property Exclude array.
  
Ignore os erros de MAPI_E_COMPUTED retornados na estrutura **SPropProblemArray** no parâmetro _lppProblems_ . 
  
O identificador de interface em que _lpSrcInterface_ aponta é geralmente o mesmo que o identificador de interface que o _lpDestInterface_ aponta. 
  
Se você passar um identificador de interface aceitável no _lpDestInterface_ , mas um ponteiro inválido no _lpDestObj_, os resultados serão imprevisíveis. Provavelmente isso causará falha no provedor. 
  
Por outro lado, se você estiver ciente de informações complementares que não devem ser copiadas ou movidas, adicione os identificadores de interface para as interfaces a serem excluídas na matriz passadas no parâmetro _rgiidExclude_ . Por exemplo, se você estiver copiando mensagens, mas não qualquer um de seus anexos de mensagem, passe IID_IMessage na matriz _rgiidExclude_ . **** Docopyto ignora todas as interfaces listadas no _rgiidExclude_ que não são reconhecidas. 
  
Quando você usa o parâmetro _rgiidExclude_ para excluir uma interface, ele também exclui todas as interfaces derivadas dessa interface. Por exemplo, a exclusão da interface [IMAPIContainer](imapicontainerimapiprop.md) faz com que as pastas ou contêineres do catálogo de endereços sejam excluídos, dependendo do tipo de provedor. Não exclua [IMAPIProp](imapipropiunknown.md) ou [IUnknown](https://msdn.microsoft.com/library/33f1d79a-33fc-4ce5-a372-e08bda378332%28Office.15%29.aspx) , pois muitas interfaces derivam deles. 
  
 **** Docopyto relata erros globais que se aplicam à operação como um todo e erros individuais que se aplicam a propriedades individuais. Esses erros individuais são colocados em uma estrutura **SPropProblemArray** . Você pode suprimir o relatório de erros no nível da propriedade passando NULL, em vez de um ponteiro válido, para o parâmetro da estrutura da matriz do problema da propriedade. 
  
Se você quiser receber informações sobre erros, passe um ponteiro de estrutura **SPropProblemArray** válido no parâmetro _lppProblems_ . Quando **** docopyto retorna S_OK, verifique se há possíveis erros com propriedades individuais na estrutura. Quando **** docopyto retorna um erro, nenhuma informação é retornada na estrutura **SPropProblemArray** . Em vez disso, chame o método [IMAPISupport:: GetLastError](imapisupport-getlasterror.md) para recuperar informações de erro detalhadas. 
  
Se **** docopyto retornar S_OK, libere a estrutura **SPropProblemArray** retornada chamando a função [MAPIFreeBuffer](mapifreebuffer.md) . 
  
Se ocorrer um erro global na chamada **** docopyto, não use nem libere a estrutura **SPropProblemArray** . Os provedores devem ignorar o membro _ulIndex_ nas estruturas **SPropProblemArray** retornadas por docopyto. ****
  
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

