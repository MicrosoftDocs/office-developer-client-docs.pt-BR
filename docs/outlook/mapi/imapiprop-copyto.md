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
description: '�ltima altera��o: segunda-feira, 9 de mar�o de 2015'
ms.openlocfilehash: aa2869b1e3495bfb8a431e79a55d11a1ee1c5ca6
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19767141"
---
# <a name="imapipropcopyto"></a>IMAPIProp::CopyTo

  
  
**Aplica-se a**: Outlook 
  
Copia ou move todas as propriedades, exceto especificamente propriedades excluídas.
  
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

## <a name="parameters"></a>Par�metros

 _ciidExclude_
  
> [in] A contagem de interfaces a serem excluídos quando as propriedades são copiadas ou movidas.
    
 _rgiidExclude_
  
> [in] Uma matriz de identificadores de interface (IIDs) que especificam as interfaces que não devem ser usados quando informações complementares são copiadas ou movidas para o objeto de destino.
    
 _lpExcludeProps_
  
> [in] Um ponteiro para uma matriz de marca de propriedade que identifica as marcas de propriedade que devem ser excluídas da cópia ou a operação de movimentação. Passando o parâmetro _lpExcludeProps_ **Nulo** indica que todas as propriedades do objeto devem ser copiadas ou movidas. **CopyTo** retorna MAPI_E_INVALID_PARAMETER quando o membro **cValues** da estrutura [SPropProblemArray](spropproblemarray.md) apontado pela _lpExcludeProps_ estiver definido como 0. 
    
 _ulUIParam_
  
> [in] Um identificador para a janela pai do indicador de progresso. 
    
 _lpProgress_
  
> [in] Um ponteiro para uma implementação do indicador de progresso. Se **Nulo** é passado no parâmetro _lpProgress_ , MAPI fornece a implementação de andamento. O parâmetro _lpProgress_ é ignorado, a menos que o sinalizador MAPI_DIALOG é definido no parâmetro _ulFlags_ . 
    
 _lpInterface_
  
> [in] Um ponteiro para o identificador de interface (IID) que representa a interface que será usada para acessar o objeto apontado pelo parâmetro _lpDestObj_ . O parâmetro _lpInterface_ não deve ser **nula**.
    
 _lpDestObj_
  
> [in] Um ponteiro para o objeto para receber as propriedades copiadas ou movidas.
    
 _ulFlags_
  
> [in] Uma bitmask dos sinalizadores que controla a operação de cópia ou movimentação. Sinalizadores a seguir podem ser definidos:
    
MAPI_DECLINE_OK 
  
> Se **CopyTo** chama o método [IMAPISupport::DoCopyTo](imapisupport-docopyto.md) para lidar com a cópia ou a operação de movimentação, ele em vez disso, deve retornar imediatamente com o valor de erro MAPI_E_DECLINE_COPY. O sinalizador MAPI_DECLINE_OK é definido por MAPI para limitar a recursão. Os clientes não definir esse sinalizador. 
    
MAPI_DIALOG 
  
> Exibe um indicador de progresso.
    
MAPI_MOVE 
  
> **CopyTo** deve realizar uma operação de movimentação, em vez de uma operação de cópia. Quando esse sinalizador não estiver definida, **CopyTo** executa uma operação de cópia. 
    
MAPI_NOREPLACE 
  
> Propriedades existentes no objeto de destino não devem ser substituídas. Quando esse sinalizador não estiver definida, **CopyTo** substitui as propriedades existentes. 
    
 _lppProblems_
  
> [além, out] Na entrada, um ponteiro para um ponteiro para uma estrutura **SPropProblemArray** ; Caso contrário, **null**, indicando sem a necessidade de informações de erro. Se _lppProblems_ for um ponteiro válido na entrada, **CopyTo** retorna informações detalhadas sobre erros no copiando uma ou mais propriedades. 
    
## <a name="return-value"></a>Valor retornado

S_OK 
  
> As propriedades foi copiadas ou movidas com êxito.
    
MAPI_E_COLLISION 
  
> Não é possível copiar um Subobjeto porque um Subobjeto com o mesmo nome para exibição — especificado pela propriedade **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) — já existe no objeto de destino. 
    
MAPI_E_DECLINE_COPY 
  
> O provedor de serviços não implementa a operação de cópia.
    
MAPI_E_FOLDER_CYCLE 
  
> O objeto de origem executando a operação de cópia ou movimentação direta ou indiretamente contém o objeto de destino. Trabalho significativo pode ter sido executado antes que esta condição foi descoberta, para que os objetos de origem e destino podem ser modificados parcialmente. 
    
MAPI_E_INTERFACE_NOT_SUPPORTED 
  
> Não há suporte para a interface identificada pelo parâmetro _lpInterface_ pelo objeto de destino. 
    
MAPI_E_NO_ACCESS 
  
> Foi feita uma tentativa de acessar um objeto para o qual o chamador tem permissões insuficientes. Esse erro será retornado se o objeto de destino é o mesmo que o objeto de origem.
    
Os seguintes valores podem ser retornados na estrutura de **SPropProblemArray** , mas não como valores de retorno para **CopyTo**. Os seguintes erros se aplicam a uma única propriedade:
  
MAPI_E_BAD_CHARWIDTH 
  
> Tanto o sinalizador MAPI_UNICODE foi definido e **CopyTo** não oferece suporte a Unicode, ou MAPI_UNICODE não foi definido e **CopyTo** suporta somente Unicode. 
    
MAPI_E_COMPUTED 
  
> A propriedade não pode ser modificada pelo chamador porque ele é uma propriedade somente leitura, computada pelo proprietário do objeto de destino. Esse erro não é grave; o chamador deve permitir que a operação de cópia continuar.
    
MAPI_E_INVALID_TYPE 
  
> O tipo de propriedade é inválido.
    
MAPI_E_UNEXPECTED_TYPE 
  
> O tipo de propriedade não é o tipo esperado pelo chamador.
    
## <a name="remarks"></a>Coment�rios

Por padrão, o método **IMAPIProp::CopyTo** copia ou move todas as propriedades do objeto atual a um objeto de destino. **CopyTo** é usado quando um objeto deve ser copiado ou movido exatamente, com todos ou a maioria de suas propriedades intactas. 
  
Qualquer subobjetos no objeto de origem automaticamente estão incluídos na operação e são copiados ou movidos na íntegra. Por padrão, **CopyTo** substitui quaisquer propriedades no objeto de destino que corresponde às propriedades do objeto de origem. Se qualquer uma das propriedades movidas ou copiadas já existir no objeto de destino, as propriedades existentes são sobrescritas por novas propriedades, exceto se o sinalizador MAPI_NOREPLACE estiver definido no parâmetro _ulFlags_ . As informações existentes no objeto de destino que não será substituído são permanecem inalteradas. 
  
## <a name="notes-to-implementers"></a>Notas para implementadores

Você pode fornecer uma implementação total de **CopyTo** ou baseiam-se na implementação de MAPI fornece em seu objeto de suporte. Se você quiser usar a implementação de MAPI, chame **IMAPISupport::DoCopyTo**. No entanto, se você delega o processamento para **DoCopyTo** e você é passadas o sinalizador MAPI_DECLINE_OK, evitar a chamada de suporte e retornar MAPI_E_DECLINE_COPY em vez disso. MAPI chamará com esse sinalizador para evitar a recursão possível que pode acontecer quando as pastas são copiadas. 
  
Como a operação de cópia pode ser demorada, você deve exibir um indicador de progresso. Use a implementação de [IMAPIProgress](imapiprogressiunknown.md) passada no parâmetro _lpProgress_ , se houver uma. Se _lpProgress_ for **nula**, chame o método de [IMAPISupport::DoProgressDialog](imapisupport-doprogressdialog.md) para usar a implementação de MAPI. 
  
Não tente definir quaisquer propriedades conhecidas de somente leitura no objeto de destino; retorne MAPI_E_NO_ACCESS em vez disso.
  
Os objetos de origem e destino devem usar as mesmas interfaces. Retorne MAPI_E_INVALID_PARAMETER se _lpInterface_ não estiver definida. 
  
Retorne MAPI_E_INTERFACE_NOT_SUPPORTED se todas as interfaces conhecidas serão excluídas.
  
## <a name="notes-to-callers"></a>Notas para chamadores

Não definir o sinalizador MAPI_DECLINE_OK; MAPI usa em suas chamadas para implementações de **CopyTo** do provedor de repositório de mensagem. 
  
Porque as operações de movimentação e cópia podem demorar, você deve solicitar a exibição de um indicador de progresso, definindo o sinalizador MAPI_DIALOG. Você pode definir o parâmetro _lpProgress_ à sua implementação do **IMAPIProgress**, se você tiver um, ou como **Nulo**. Se _lpProgress_ for **nula**, **CopyTo** usará o indicador de progresso padrão que fornece de MAPI. 
  
Você pode suprimir a exibição de um indicador de progresso, não definindo o sinalizador MAPI_DIALOG. **CopyTo** irá ignorar os parâmetros _ulUIParam_ e _lpProgress_ e não exibirá o indicador. 
  
 **CopyTo** possível denunciar global e individual ou erros que ocorrem com uma ou mais propriedades. Esses erros individuais são colocados em uma estrutura **SPropProblemArray** . Você pode suprimir relatório no nível de propriedade passando **Nulo**, em vez de um ponteiro válido, para o parâmetro de estrutura de matriz de problema de propriedade de erros. 
  
Se você desejar receber informações sobre erros, passe um ponteiro de estrutura de **SPropProblemArray** válido no parâmetro _lppProblems_ . Quando **CopyTo** Retorna S_OK, verifique se há erros possíveis com as propriedades individuais na estrutura. Quando **CopyTo** retornará um erro, nenhuma informação é retornada na estrutura **SPropProblemArray** . Em vez disso, chame [IMAPIProp::GetLastError](imapiprop-getlasterror.md) para recuperar informações de erro detalhadas. 
  
Se **CopyTo** Retorna S_OK, livre a estrutura de **SPropProblemArray** retornada ao chamar a função [MAPIFreeBuffer](mapifreebuffer.md) . 
  
Se você copiar propriedades que são exclusivas para o tipo de objeto de origem, certifique-se de que o objeto de destino é do mesmo tipo. **CopyTo** não impede que você associar propriedades que geralmente pertencem a um tipo de objeto com outro tipo de objeto. Cabe a você copie as propriedades que fazem sentido para o objeto de destino. Por exemplo, você não deve copiar propriedades da mensagem para um contêiner de catálogo de endereços. 
  
Para garantir que você copie entre os objetos do mesmo tipo, verifique se o objeto de origem e destino são do mesmo tipo, por comparando ponteiros de objeto ou chamar [IUnknown:: QueryInterface](http://msdn.microsoft.com/en-us/library/ms682521%28v=VS.85%29.aspx). Defina o identificador de interface apontado pela _lpInterface_ para a interface padrão para o objeto de origem. Além disso, certifique-se de que o tipo de objeto ou a propriedade **PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md)) é o mesmo para os dois objetos. Por exemplo, se você copiar de uma mensagem, defina _lpInterface_ IID_IMessage e o **PR_OBJECT_TYPE** para ambos os objetos para MAPI_MESSAGE. 
  
Se um ponteiro inválido é passado no parâmetro _lpDestObj_ , os resultados serão imprevisíveis. 
  
Excluindo propriedades em uma chamada **CopyTo** pode ser útil. Por exemplo, alguns objetos têm propriedades que são específicas para uma única instância do objeto, a data e hora da entrega da mensagem. Para evitar copiando o tempo de entrega da mensagem quando você copia a mensagem para uma pasta diferente, especifique **PR_MESSAGE_DELIVERY_TIME** ([PidTagMessageDeliveryTime](pidtagmessagedeliverytime-canonical-property.md)) na matriz propriedade tag exclude. Para excluir a lista de destinatários da mensagem, adicione a propriedade **PR_MESSAGE_RECIPIENTS** ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md)) à matriz exclude. Para excluir anexos da mensagem, adicione a propriedade **PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md)) à matriz.
  
Impedir da mesma forma, as cópias ou movimentações de uma pasta ou da tabela de hierarquia ou conteúdo do contêiner de catálogo de endereços, incluindo **PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md)) ou **PR_CONTAINER_CONTENTS** ([ PidTagContainerContents](pidtagcontainercontents-canonical-property.md)) na propriedade tag Excluir matriz.
  
Para excluir propriedades da cópia ou operação de movimentação, inclua suas marcas de propriedade no parâmetro _lpExcludeProps_ . Se você passar os resultados da macro **PROP_TAG** para criar uma marca de propriedade de um identificador específico na matriz de marca de propriedade, todas as propriedades com esse identificador não serão excluídas. Por exemplo, a seguinte entrada na matriz de marca de propriedade faz com que todas as propriedades com um identificador do 0x8002 sejam excluídos, independentemente do tipo: 
  
 `PROP_TAG(PT_LONG, 0x8002)`
  
A marca de propriedade **PR_NULL** ([PidTagNull](pidtagnull-canonical-property.md)) não pode ser incluída na matriz _lpExcludeProps_ . 
  
A utilidade do recurso **CopyTo** para excluindo interfaces talvez não é tão óbvia como a utilidade dos excluindo propriedades. Você pode excluir uma interface quando você copia a um objeto que não tem conhecimento de um grupo de propriedades. Por exemplo, se você copiar propriedades de uma pasta em um anexo, as únicas propriedades que o anexo pode trabalhar com são as propriedades genéricas disponíveis com qualquer implementação [IMAPIProp](imapipropiunknown.md) . Excluindo [IMAPIFolder](imapifolderimapicontainer.md) da operação de cópia, o anexo não receberá qualquer uma das propriedades de pasta mais específicas. 
  
Quando você usa o parâmetro _rgiidExclude_ para excluir uma interface, ele também exclui todas as interfaces derivadas essa interface. Por exemplo, excluir [IMAPIContainer](imapicontainerimapiprop.md) faz com que pastas ou contêineres de catálogo de endereços a serem excluídos, dependendo do tipo de provedor. Não exclua **IMAPIProp** ou [IUnknown](http://msdn.microsoft.com/en-us/library/ms680509%28v=VS.85%29.aspx) porque tantas interfaces derivam deles. 
  
Ignorar MAPI_E_COMPUTED erros retornados na estrutura de **SPropProblemArray** no parâmetro _lppProblems_ . 
  
## <a name="mfcmapi-reference"></a>Referência MFCMAPI

Para exemplos de código MFCMAPI, consulte a tabela a seguir.
  
|**Arquivo**|**Function**|**Comment**|
|:-----|:-----|:-----|
|CPP  <br/> |LoadFromMSG  <br/> |MFCMAPI usa o método **IMAPIProp::CopyTo** para copiar as propriedades de um arquivo. msg a um objeto [IMAPIMessageSite](imapimessagesiteiunknown.md) .  <br/> |
|FolderDlg.cpp  <br/> |CFolderDlg::HandlePaste  <br/> |MFCMAPI usa o método **IMAPIProp::CopyTo** para copiar propriedades de uma mensagem de origem para uma mensagem de destino durante uma operação de colar.  <br/> |
   
## <a name="see-also"></a>Confira também



[IMAPIFolder::CopyMessages](imapifolder-copymessages.md)
  
[IMAPIProp::GetLastError](imapiprop-getlasterror.md)
  
[IMAPIMessageSite: IUnknown](imapimessagesiteiunknown.md)
  
[IMAPIProgress: IUnknown](imapiprogressiunknown.md)
  
[IMAPISupport::DoProgressDialog](imapisupport-doprogressdialog.md)
  
[IMAPISupport::DoCopyTo](imapisupport-docopyto.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[Propriedade canônico de PidTagContainerContents](pidtagcontainercontents-canonical-property.md)
  
[Propriedade canônico de PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md)
  
[Propriedade canônico de PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md)
  
[Propriedade canônico de PidTagMessageDeliveryTime](pidtagmessagedeliverytime-canonical-property.md)
  
[Propriedade canônico de PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md)
  
[Propriedade canônico de PidTagObjectType](pidtagobjecttype-canonical-property.md)
  
[SPropProblemArray](spropproblemarray.md)
  
[SPropTagArray](sproptagarray.md)
  
[IMAPIProp: IUnknown](imapipropiunknown.md)


[MFCMAPI como um exemplo de código](mfcmapi-as-a-code-sample.md)

