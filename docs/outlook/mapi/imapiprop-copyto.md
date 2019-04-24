---
title: IMAPIPropCopyTo
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIProp.CopyTo
api_type:
- COM
ms.assetid: e56042e9-5bb7-4a99-b6de-1546d4ca07f0
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: f76b0a5482647fe3e181a36d7dcd8cb60ffc8985
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32356389"
---
# <a name="imapipropcopyto"></a>IMAPIProp::CopyTo

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Copia ou move todas as propriedades, exceto as propriedades especificamente excluídas.
  
```cpp
HRESULT CopyTo(
 ULONG ciidExclude,
 LPCIID rgiidExclude,
 LPSPropTagArray lpExcludeProps,
 ULONG_PTR ulUIParam,
 LPMAPIPROGRESS lpProgress,
 LPCIID lpInterface,
 LPVOID lpDestObj,
 ULONG ulFlags,
 LPSPropProblemArray FAR * lppProblems
);
```

## <a name="parameters"></a>Parâmetros

 _ciidExclude_
  
> no A contagem de interfaces a serem excluídas quando as propriedades são copiadas ou movidas.
    
 _rgiidExclude_
  
> no Uma matriz de identificadores de interface (IIDs) que especificam interfaces que não devem ser usadas quando as informações suplementares são copiadas ou movidas para o objeto de destino.
    
 _lpExcludeProps_
  
> no Um ponteiro para uma matriz de marca de propriedade que identifica as marcas de propriedade que devem ser excluídas da operação de cópia ou movimentação. Passar **NULL** no parâmetro _lpExcludeProps_ indica que todas as propriedades do objeto devem ser copiadas ou movidas. **CopyTo** retorna MAPI_E_INVALID_PARAMETER quando o membro **CValues** da estrutura [SPropProblemArray](spropproblemarray.md) apontada por _lpExcludeProps_ é definida como 0. 
    
 _ulUIParam_
  
> no Uma alça para a janela pai do indicador de progresso. 
    
 _lpProgress_
  
> no Um ponteiro para uma implementação de indicador de progresso. Se **NULL** for passado no parâmetro _lpProgress_ , MAPI fornecerá a implementação de progresso. O parâmetro _lpProgress_ é ignorado, a menos que o sinalizador MAPI_DIALOG esteja definido no parâmetro _parâmetroulflags_ . 
    
 _lpInterface_
  
> no Um ponteiro para o identificador de interface (IID) que representa a interface a ser usada para acessar o objeto apontado pelo parâmetro _lpDestObj_ . O parâmetro _lpInterface_ não deve ser **nulo**.
    
 _lpDestObj_
  
> no Um ponteiro para o objeto para receber as propriedades copiadas ou movidas.
    
 _ulFlags_
  
> no Uma bitmask de sinalizadores que controlam a operação de cópia ou movimentação. Os seguintes sinalizadores podem ser definidos:
    
MAPI_DECLINE_OK 
  
> Se **CopyTo** chamar o método [IMAPISupport::D ocopyto](imapisupport-docopyto.md) para manipular a operação de cópia ou movimentação, ele deverá retornar imediatamente com o valor de erro MAPI_E_DECLINE_COPY. O sinalizador MAPI_DECLINE_OK é definido por MAPI para limitar a recursividade. Os clientes não definem esse sinalizador. 
    
MAPI_DIALOG 
  
> Exibe um indicador de progresso.
    
MAPI_MOVE 
  
> **CopyTo** deve executar uma operação de movimentação em vez de uma operação de cópia. Quando esse sinalizador não é definido, **CopyTo** executa uma operação de cópia. 
    
MAPI_NOREPLACE 
  
> As propriedades existentes no objeto de destino não devem ser substituídas. Quando esse sinalizador não é definido, **CopyTo** substitui as propriedades existentes. 
    
 _lppProblems_
  
> [in, out] Na entrada, um ponteiro para um ponteiro para uma estrutura **SPropProblemArray** ; caso contrário, **NULL**, indicando que não há necessidade de informações de erro. Se _lppProblems_ for um ponteiro válido na entrada, **CopyTo** retornará informações detalhadas sobre erros ao copiar uma ou mais propriedades. 
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> As propriedades foram copiadas ou movidas com êxito.
    
MAPI_E_COLLISION 
  
> Um subobjeto não pode ser copiado porque um subobjeto com o mesmo nome de exibição, especificado pela propriedade **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)), já existe no objeto de destino. 
    
MAPI_E_DECLINE_COPY 
  
> O provedor de serviços não implementa a operação de cópia.
    
MAPI_E_FOLDER_CYCLE 
  
> O objeto de origem executando a operação copiar ou mover direta ou indiretamente contém o objeto de destino. Um trabalho significativo pode ter sido realizado antes da descoberta dessa condição, portanto, os objetos de origem e de destino podem ser parcialmente modificados. 
    
MAPI_E_INTERFACE_NOT_SUPPORTED 
  
> A interface identificada pelo parâmetro _lpInterface_ não é suportada pelo objeto de destino. 
    
MAPI_E_NO_ACCESS 
  
> Foi feita uma tentativa de acessar um objeto para o qual o chamador tem permissões insuficientes. Esse erro será retornado se o objeto de destino for o mesmo que o objeto de origem.
    
Os valores a seguir podem ser retornados na estrutura **SPropProblemArray** , mas não como valores de retorno para **CopyTo**. Os seguintes erros se aplicam a uma única propriedade:
  
MAPI_E_BAD_CHARWIDTH 
  
> O sinalizador MAPI_UNICODE foi definido e **CopyTo** não dá suporte a Unicode, ou o MAPI_UNICODE não foi definido e o **CopyTo** suporta apenas Unicode. 
    
MAPI_E_COMPUTED 
  
> A propriedade não pode ser modificada pelo chamador porque é uma propriedade somente leitura, calculada pelo proprietário do objeto de destino. Esse erro não é grave; o chamador deve permitir que a operação de cópia continue.
    
MAPI_E_INVALID_TYPE 
  
> O tipo de propriedade é inválido.
    
MAPI_E_UNEXPECTED_TYPE 
  
> O tipo de propriedade não é o tipo esperado pelo chamador.
    
## <a name="remarks"></a>Comentários

Por padrão, o método **IMAPIProp:: CopyTo** copia ou move todas as propriedades do objeto atual para um objeto de destino. **CopyTo** é usado quando um objeto deve ser copiado ou movido exatamente, com todas ou a maioria de suas propriedades intacta. 
  
Todos os subobjetos no objeto de origem são automaticamente incluídos na operação e são copiados ou movidos completamente. Por padrão, **CopyTo** substitui quaisquer propriedades no objeto de destino que correspondam às propriedades do objeto de origem. Se qualquer uma das propriedades copiadas ou movidas já existir no objeto de destino, as propriedades existentes serão sobrescritas pelas novas propriedades, a menos que o sinalizador MAPI_NOREPLACE seja definido no parâmetro _parâmetroulflags_ . As informações existentes no objeto de destino que não estão sobrescritas são deixadas inalteradas. 
  
## <a name="notes-to-implementers"></a>Observações para implementadores

Você pode fornecer uma implementação completa de **CopyTo** ou depender da implementação que a MAPI fornece em seu objeto support. Se você quiser usar a implementação MAPI, chame **IMAPISupport::D ocopyto**. No enTanto, se você fizer o **** processamento de representante para docopyto e passar o sinalizador MAPI_DECLINE_OK, evite a chamada de suporte e retorne MAPI_E_DECLINE_COPY. O MAPI chamará com esse sinalizador para evitar a possível recursão que pode ocorrer quando pastas são copiadas. 
  
Como a operação de cópia pode ser demorada, você deve exibir um indicador de progresso. Use a implementação [método imapiprogress](imapiprogressiunknown.md) passada no parâmetro _lpProgress_ , se houver um. Se _lpProgress_ for **NULL**, chame o método [IMAPISupport::D OPROGRESSDIALOG](imapisupport-doprogressdialog.md) para usar a implementação MAPI. 
  
Não tente definir nenhuma propriedade somente leitura conhecida no objeto de destino; em vez disso, retorne MAPI_E_NO_ACCESS.
  
Os objetos de origem e destino devem usar as mesmas interfaces. Retornar MAPI_E_INVALID_PARAMETER se _lpInterface_ não estiver definido. 
  
Retornar MAPI_E_INTERFACE_NOT_SUPPORTED se todas as interfaces conhecidas forem excluídas.
  
## <a name="notes-to-callers"></a>Notas para chamadores

Não defina o sinalizador MAPI_DECLINE_OK; MAPI usa-o em suas chamadas para implementações **CopyTo** de provedor de repositório de mensagens. 
  
Como as operações de cópia e movimentação podem demorar um pouco, você deve solicitar a exibição de um indicador de progresso Configurando o sinalizador MAPI_DIALOG. Você pode definir o parâmetro _lpProgress_ para sua implementação do **método imapiprogress**, se você tiver um, ou como **nulo**. Se _lpProgress_ for **NULL**, **CopyTo** usará o indicador de progresso padrão que o MAPI fornece. 
  
Você pode suprimir a exibição de um indicador de progresso não definindo o sinalizador MAPI_DIALOG. **CopyTo** ignorará os parâmetros _ulUIParam_ e _lpProgress_ e não exibirá o indicador. 
  
 **CopyTo** pode relatar erros globais e individuais, ou erros que ocorrem com uma ou mais propriedades. Esses erros individuais são colocados em uma estrutura **SPropProblemArray** . Você pode suprimir o relatório de erros no nível da propriedade passando **NULL**, em vez de um ponteiro válido, para o parâmetro da estrutura da matriz do problema da propriedade. 
  
Se você quiser receber informações sobre erros, passe um ponteiro de estrutura **SPropProblemArray** válido no parâmetro _lppProblems_ . Quando **CopyTo** retornar S_OK, verifique possíveis erros com propriedades individuais na estrutura. Quando **CopyTo** retorna um erro, nenhuma informação é retornada na estrutura **SPropProblemArray** . Em vez disso, chame [IMAPIProp:: GetLastError](imapiprop-getlasterror.md) para recuperar informações de erro detalhadas. 
  
Se **CopyTo** retornar S_OK, libere a estrutura **SPropProblemArray** retornada chamando a função [MAPIFreeBuffer](mapifreebuffer.md) . 
  
Se você copiar propriedades que são exclusivas para o tipo de objeto de origem, você deve garantir que o objeto de destino seja do mesmo tipo. **CopyTo** não impede que você associe propriedades que normalmente pertencem a um tipo de objeto com outro tipo de objeto. Você pode copiar propriedades que fazem sentido para o objeto de destino. Por exemplo, você não deve copiar as propriedades de mensagem para um contêiner de catálogo de endereços. 
  
Para garantir que você copie entre objetos do mesmo tipo, verifique se o objeto de origem e destino são do mesmo tipo, comparando ponteiros de objeto ou chamando [IUnknown:: QueryInterface](https://msdn.microsoft.com/library/ms682521%28v=VS.85%29.aspx). Defina o identificador de interface apontado por _lpInterface_ para a interface padrão do objeto de origem. Além disso, certifique-se de que o tipo de objeto ou a propriedade **PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md)) seja a mesma dos dois objetos. Por exemplo, se você copiar de uma mensagem, defina _lpInterface_ como IID_IMessage e o **PR_OBJECT_TYPE** para ambos os objetos como MAPI_MESSAGE. 
  
Se um ponteiro inválido for passado no parâmetro _lpDestObj_ , os resultados serão imprevisíveis. 
  
Excluir propriedades em uma chamada **CopyTo** pode ser útil. Por exemplo, alguns objetos têm propriedades específicas para uma única instância do objeto, como data e hora da entrega da mensagem. Para evitar a cópia do tempo de entrega de uma mensagem quando você copia a mensagem para uma pasta diferente, especifique **PR_MESSAGE_DELIVERY_TIME** ([PidTagMessageDeliveryTime](pidtagmessagedeliverytime-canonical-property.md)) na marca de propriedade Exclude array. Para excluir a lista de destinatários de uma mensagem, adicione a propriedade **PR_MESSAGE_RECIPIENTS** ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md)) à matriz Exclude. Para excluir os anexos de uma mensagem, adicione a propriedade **PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md)) à matriz.
  
Da mesma forma, evite a cópia ou a movimentação de uma pasta ou hierarquia de um contêiner de catálogo de endereços ou uma tabela de conteúdo incluindo **PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md)) ou **PR_CONTAINER_CONTENTS** ([ PidTagContainerContents](pidtagcontainercontents-canonical-property.md)) na marca Property Exclude array.
  
Para excluir propriedades da operação de cópia ou movimentação, inclua suas marcas de propriedade no parâmetro _lpExcludeProps_ . Se você passar os resultados da macro **PROP_TAG** para criar uma marca de propriedade a partir de um identificador específico na matriz de marca de propriedade, todas as propriedades com esse identificador serão excluídas. Por exemplo, a seguinte entrada na matriz de marca de propriedade faz com que todas as propriedades com um identificador de 0x8002 sejam excluídas, independentemente do tipo: 
  
 `PROP_TAG(PT_LONG, 0x8002)`
  
A marca de propriedade **PR_NULL** ([PidTagNull](pidtagnull-canonical-property.md)) não pode ser incluída na matriz _lpExcludeProps_ . 
  
A utilidade do recurso **CopyTo** para excluir interfaces talvez não seja tão óbvia quanto a utilidade de excluir propriedades. Você pode excluir uma interface ao copiar para um objeto que não tenha conhecimento de um grupo de propriedades. Por exemplo, se você copiar propriedades de uma pasta para um anexo, as únicas propriedades com as quais o anexo pode trabalhar são as propriedades genéricas disponíveis em qualquer implementação do [IMAPIProp](imapipropiunknown.md) . Ao excluir [IMAPIFolder](imapifolderimapicontainer.md) da operação de cópia, o anexo não receberá nenhuma das propriedades de pasta mais específicas. 
  
Quando você usa o parâmetro _rgiidExclude_ para excluir uma interface, ele também exclui todas as interfaces derivadas dessa interface. Por exemplo, a exclusão de [IMAPIContainer](imapicontainerimapiprop.md) faz com que as pastas ou contêineres do catálogo de endereços sejam excluídos, dependendo do tipo de provedor. Não exclua **IMAPIProp** ou [IUnknown](https://msdn.microsoft.com/library/ms680509%28v=VS.85%29.aspx) , pois muitas interfaces derivam deles. 
  
Ignore os erros de MAPI_E_COMPUTED retornados na estrutura **SPropProblemArray** no parâmetro _lppProblems_ . 
  
## <a name="mfcmapi-reference"></a>Referência do MFCMAPI

Para ver códigos de exemplo do MFCMAPI, confira a tabela a seguir.
  
|**Arquivo**|**Função**|**Comentário**|
|:-----|:-----|:-----|
|Arquivo. cpp  <br/> |LoadFromMSG  <br/> |MFCMAPI usa o método **IMAPIProp:: CopyTo** para copiar as propriedades de um arquivo. msg para um objeto [IMAPIMessageSite](imapimessagesiteiunknown.md) .  <br/> |
|FolderDlg. cpp  <br/> |CFolderDlg:: HandlePaste  <br/> |MFCMAPI usa o método **IMAPIProp:: CopyTo** para copiar as propriedades de uma mensagem de origem para uma mensagem de destino durante uma operação de colagem.  <br/> |
   
## <a name="see-also"></a>Confira também



[IMAPIFolder::CopyMessages](imapifolder-copymessages.md)
  
[IMAPIProp::GetLastError](imapiprop-getlasterror.md)
  
[IMAPIMessageSite : IUnknown](imapimessagesiteiunknown.md)
  
[IMAPIProgress : IUnknown](imapiprogressiunknown.md)
  
[IMAPISupport::DoProgressDialog](imapisupport-doprogressdialog.md)
  
[IMAPISupport::DoCopyTo](imapisupport-docopyto.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[Propriedade canônica PidTagContainerContents](pidtagcontainercontents-canonical-property.md)
  
[Propriedade canônica PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md)
  
[Propriedade canônica PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md)
  
[Propriedade canônica PidTagMessageDeliveryTime](pidtagmessagedeliverytime-canonical-property.md)
  
[Propriedade canônica PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md)
  
[Propriedade canônica PidTagObjectType](pidtagobjecttype-canonical-property.md)
  
[SPropProblemArray](spropproblemarray.md)
  
[SPropTagArray](sproptagarray.md)
  
[IMAPIProp : IUnknown](imapipropiunknown.md)


[MFCMAPI como exemplo de código](mfcmapi-as-a-code-sample.md)

