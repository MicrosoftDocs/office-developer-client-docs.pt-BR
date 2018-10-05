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
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 6f6c802f1d5ead1750c05fafc54533487fe3732a
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25390629"
---
# <a name="imapisupportdocopyto"></a>IMAPISupport::DoCopyTo

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Copia ou move todas as propriedades de um objeto, exceto propriedades especificamente excluídas, a outro objeto.
  
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
  
> [in] Um ponteiro para o identificador de interface (IID) que representa a interface que será usada para acessar o objeto que tem as propriedades devem ser copiados ou movidos.
    
 _lpSrcObj_
  
> [in] Um ponteiro para o objeto que tem as propriedades devem ser copiados ou movidos.
    
 _ciidExclude_
  
> [in] A contagem de interfaces a serem excluídos quando você copiar ou mover propriedades.
    
 _rgiidExclude_
  
> [in] Uma matriz de identificadores de interface que indica as interfaces que não devem ser usados ao copiar ou mover informações complementares para o objeto de destino.
    
 _lpExcludeProps_
  
> [in] Um ponteiro para uma matriz de marca de propriedade que identifica as marcas de propriedade que devem ser excluídas da cópia ou a operação de movimentação. Passar NULL no parâmetro _lpExcludeProps_ indica que todas as propriedades do objeto devem ser copiadas ou movidas. **DoCopyTo** retorna MAPI_E_INVALID_PARAMETER quando o membro **cValues** da estrutura [SPropTagArray](sproptagarray.md) apontado pela _lpExcludeProps_ estiver definido como 0. 
    
 _ulUIParam_
  
> [in] Um identificador para a janela pai do indicador de progresso. 
    
 _lpProgress_
  
> [in] Um ponteiro para uma implementação do indicador de progresso. Se NULL é passada no parâmetro _lpProgress_ , MAPI fornece a implementação de andamento. O parâmetro _lpProgress_ é ignorado, a menos que o sinalizador MAPI_DIALOG é definido no parâmetro _ulFlags_ . 
    
 _lpDestInterface_
  
> [in] Um ponteiro para o identificador de interface que representa a interface que será usada para acessar o objeto para receber as propriedades copiadas ou movidas.
    
 _lpDestObj_
  
> [in] Um ponteiro para o objeto para receber as propriedades copiadas ou movidas.
    
 _ulFlags_
  
> [in] Uma bitmask dos sinalizadores que controla a operação de cópia ou movimentação. Sinalizadores a seguir podem ser definidos:
    
MAPI_DIALOG 
  
> Exibe um indicador de progresso. 
    
MAPI_MOVE 
  
> **DoCopyTo** deve realizar uma operação de movimentação, em vez de uma operação de cópia. Quando esse sinalizador não estiver definida, **DoCopyTo** executa uma operação de cópia. 
    
MAPI_NOREPLACE 
  
> Propriedades existentes no objeto de destino não devem ser substituídas. Quando esse sinalizador não estiver definida, **DoCopyTo** substitui as propriedades existentes. 
    
 _lppProblems_
  
> [out] Na entrada, um ponteiro para um ponteiro para uma estrutura [SPropProblemArray](spropproblemarray.md) ; Caso contrário, NULL, que indica que não há necessidade de informações de erro. Se _lppProblems_ for um ponteiro válido na entrada, **DoCopyTo** retorna informações detalhadas sobre erros no copiando uma ou mais propriedades. 
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> As propriedades foi copiadas ou movidas com êxito.
    
MAPI_E_COLLISION 
  
> Uma propriedade devem ser copiados ou movidos já existe no objeto de destino e o sinalizador MAPI_NOREPLACE está definido. 
    
MAPI_E_FOLDER_CYCLE 
  
> O objeto de origem direta ou indiretamente contém o objeto de destino. Trabalho significativo pode ter sido executado antes que esta condição foi descoberta, para que os objetos de origem e destino podem ser modificados parcialmente. 
    
MAPI_E_INTERFACE_NOT_SUPPORTED 
  
> Não há suporte para a interface identificada pelo parâmetro _lpSrcInterface_ pelo objeto apontado pela _lpSrcObj_ou não há suporte para a interface identificada pelo parâmetro _lpDestInterface_ pelo objeto apontado pela _lpDestObj _. 
    
MAPI_E_NO_ACCESS 
  
> Foi feita uma tentativa de acessar um objeto para o qual o chamador tem permissões insuficientes. Esse erro será retornado se o objeto de destino é o mesmo que o objeto de origem.
    
MAPI_E_INVALID_PARAMETER 
  
> O parâmetro _lpSrcInterface_ é nulo. 
    
Os seguintes valores podem ser retornados na estrutura de **SPropProblemArray** , mas não como valores de retorno para **DoCopyTo**. Esses erros se aplicam a uma única propriedade.
  
MAPI_E_BAD_CHARWIDTH 
  
> Tanto o sinalizador MAPI_UNICODE foi definido e **DoCopyTo** não oferece suporte a Unicode, ou MAPI_UNICODE não foi definido e **DoCopyTo** suporta somente Unicode. 
    
MAPI_E_COMPUTED 
  
> A propriedade não pode ser modificada pelo chamador porque ele é uma propriedade somente leitura, computada pelo proprietário do objeto de destino. Esse erro não é grave; o chamador deve permitir que a operação de cópia continuar.
    
MAPI_E_INVALID_TYPE 
  
> O tipo de propriedade é inválido.
    
MAPI_E_UNEXPECTED_TYPE 
  
> O tipo de propriedade não é o tipo esperado pelo chamador.
    
## <a name="remarks"></a>Comentários

O método **IMAPISupport::DoCopyTo** é implementado para objetos de suporte do provedor de repositório de mensagem. Provedores de armazenamento de mensagens podem chamar **DoCopyTo** para implementar o método [IMAPIProp::CopyTo](imapiprop-copyto.md) para suas pastas e mensagens. 
  
Por padrão, o **DoCopyTo** copia ou move todas as propriedades de um objeto para um outro objeto. Qualquer subobjetos no objeto de origem automaticamente estão incluídos na operação e copiados ou movidos na íntegra. 
  
Se qualquer uma das propriedades movidas ou copiadas já existir no objeto de destino, as propriedades existentes são sobrescritas por novas propriedades, exceto se o sinalizador MAPI_NOREPLACE estiver definido no parâmetro _ulFlags_ . As informações existentes no objeto de destino que não será substituído são permanecem inalteradas. 
  
## <a name="notes-to-callers"></a>Notas para chamadores

Para excluir propriedades da cópia ou operação de movimentação, inclua suas marcas de propriedade no parâmetro _lpExcludeProps_ . Se você passar os resultados do uso de macro [PROP_TAG](prop_tag.md) para criar uma marca de propriedade de um identificador específico na matriz de marca de propriedade, todas as propriedades com esse identificador não serão excluídas. Por exemplo, a seguinte entrada na matriz de marca de propriedade faz com que todas as propriedades com um identificador do 0x8002 sejam excluídos, independentemente do tipo: 
  
 `PROP_TAG(PT_LONG, 0x8002)`
  
Para evitar copiando o tempo de entrega da mensagem quando você copia a mensagem para uma pasta diferente, especifique **PR_MESSAGE_DELIVERY_TIME** ([PidTagMessageDeliveryTime](pidtagmessagedeliverytime-canonical-property.md)) na matriz propriedade tag exclude. Para excluir a lista de destinatários da mensagem, adicione a propriedade **PR_MESSAGE_RECIPIENTS** ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md)) à matriz exclude. Para excluir anexos da mensagem, adicione a propriedade **PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md)) à matriz.
  
Da mesma forma, para evitar que as cópias ou movimentações de uma pasta ou a hierarquia do contêiner de catálogo de endereços ou a tabela de conteúdo, incluir **PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md)) ou **PR_CONTAINER_CONTENTS** ([ PidTagContainerContents](pidtagcontainercontents-canonical-property.md)) na propriedade tag Excluir matriz.
  
Ignorar MAPI_E_COMPUTED erros retornados na estrutura de **SPropProblemArray** no parâmetro _lppProblems_ . 
  
O identificador de interface _lpSrcInterface_ aponta para normalmente é o mesmo que o identificador de interface que aponta _lpDestInterface_ para. 
  
Se você passar um identificador de interface aceitável em _lpDestInterface_ , mas um ponteiro inválido no _lpDestObj_, os resultados serão imprevisíveis. Provavelmente isso fará com que seu provedor de falha. 
  
De modo oposto, se você estiver ciente informações complementares que não devem ser copiadas ou movidas, adicione os identificadores de interface para as interfaces sejam excluídos na matriz passada no parâmetro _rgiidExclude_ . Por exemplo, se você estiver copiando mensagens, mas não a qualquer um dos seus anexos da mensagem, passe IID_IMessage na matriz _rgiidExclude_ . **DoCopyTo** ignora quaisquer interfaces listadas na _rgiidExclude_ que ele não reconhece. 
  
Quando você usa o parâmetro _rgiidExclude_ para excluir uma interface, ele também exclui todas as interfaces derivadas essa interface. Por exemplo, excluindo a interface [IMAPIContainer](imapicontainerimapiprop.md) faz com que pastas ou contêineres de catálogo de endereços a serem excluídos, dependendo do tipo de provedor. Não exclua [IMAPIProp](imapipropiunknown.md) ou [IUnknown](https://msdn.microsoft.com/library/33f1d79a-33fc-4ce5-a372-e08bda378332%28Office.15%29.aspx) porque tantas interfaces derivam deles. 
  
 **DoCopyTo** relata os erros de globais que se aplicam à operação como um todo e erros individuais que se aplicam às propriedades individuais. Esses erros individuais são colocados em uma estrutura **SPropProblemArray** . Você pode suprimir relatório no nível de propriedade passando NULL, em vez de um ponteiro válido, para o parâmetro de estrutura de matriz de problema de propriedade de erros. 
  
Se você desejar receber informações sobre erros, passe um ponteiro de estrutura de **SPropProblemArray** válido no parâmetro _lppProblems_ . Quando **DoCopyTo** Retorna S_OK, verifique se há erros possíveis com as propriedades individuais na estrutura. Quando **DoCopyTo** retornará um erro, nenhuma informação é retornada na estrutura **SPropProblemArray** . Em vez disso, chame o método [IMAPISupport::GetLastError](imapisupport-getlasterror.md) para recuperar informações de erro detalhadas. 
  
Se **DoCopyTo** Retorna S_OK, livre a estrutura de **SPropProblemArray** retornada ao chamar a função [MAPIFreeBuffer](mapifreebuffer.md) . 
  
Se ocorrer um erro de global na chamada **DoCopyTo** , não use ou livre a estrutura **SPropProblemArray** . Provedores devem ignorar o membro _ulIndex_ nas estruturas **SPropProblemArray** retornado por **DoCopyTo**.
  
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

