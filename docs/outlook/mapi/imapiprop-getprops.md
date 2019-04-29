---
title: IMAPIPropGetProps
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIProp.GetProps
api_type:
- COM
ms.assetid: 1c7a9cd2-d765-4218-9aee-52df1a2aae6c
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 9b03775d495f7d1f51142eb0ed06fc9ecdf6d1a3
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33412454"
---
# <a name="imapipropgetprops"></a>IMAPIProp::GetProps

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Recupera o valor da propriedade de uma ou mais propriedades de um objeto.
  
```cpp
HRESULT GetProps(
  LPSPropTagArray lpPropTagArray,
  ULONG ulFlags,
  ULONG FAR * lpcValues,
  LPSPropValue FAR * lppPropArray
);
```

## <a name="parameters"></a>Parâmetros

 _lpPropTagArray_
  
> no Um ponteiro para uma matriz de marcas de propriedade que identificam as propriedades cujos valores devem ser recuperados. O parâmetro _lpPropTagArray_ deve ser nulo, indicando que os valores de todas as propriedades do objeto devem ser retornados ou que apontam para uma estrutura [SPropTagArray](sproptagarray.md) que contém uma ou mais marcas de propriedade. 
    
 _ulFlags_
  
> no Uma bitmask de sinalizadores que indica o formato de propriedades que têm o tipo PT_UNSPECIFIED. O seguinte sinalizador pode ser definido:
    
MAPI_UNICODE 
  
> Os valores de cadeia de caracteres dessas propriedades devem ser retornados no formato Unicode. Se o sinalizador MAPI_UNICODE não estiver definido, os valores da cadeia de caracteres deverão ser retornados no formato ANSI.
    
 _lpcValues_
  
> bota Um ponteiro para uma contagem de valores de propriedade apontados pelo parâmetro _lppPropArray_ . Se _lppPropArray_ for NULL, o conteúdo do parâmetro _lpcValues_ será zero. 
    
 _lppPropArray_
  
> bota Um ponteiro para um ponteiro para os valores de propriedade recuperados.
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> Os valores da propriedade foram recuperados com êxito.
    
MAPI_W_ERRORS_RETURNED 
  
> A chamada foi bem-sucedida, mas uma ou mais propriedades não puderam ser acessadas. O membro **aulPropTag** do valor da propriedade para cada propriedade não disponível tem um tipo de propriedade de PT_ERROR e um identificador de zero. Quando esse aviso é retornado, a chamada deve ser tratada como bem-sucedida. Para testar esse aviso, use a macro **HR_FAILED** . Para obter mais informações, consulte [usando macros para tratamento de erros](using-macros-for-error-handling.md).
    
MAPI_E_INVALID_PARAMETER 
  
> Zero foi passado no membro **cValues** da estrutura **SPropTagArray** indicada por _lpPropTagArray_.
    
## <a name="remarks"></a>Comentários

O método **IMAPIProp::** GetProps Obtém os valores de propriedade de uma ou mais propriedades de um objeto. 
  
Os valores de propriedade são retornados na mesma ordem em que foram solicitados (ou seja, a ordem das propriedades na matriz de marca de propriedade apontada por _lpPropTagArray_ corresponde à ordem na matriz de estruturas de valor de propriedade apontada por _lppPropArray _). 
  
Os tipos de propriedade especificados nos membros **aulPropTag** da matriz de marca de propriedade indicam o tipo de valor que deve ser retornado no membro **Value** de cada estrutura de valor de propriedade. No enTanto, se o chamador não souber o tipo de uma propriedade, o tipo no membro **aulPropTag** poderá ser definido em vez de PT_UNSPECIFIED. Ao recuperar o valor, getProps define o tipo correto no membro **aulPropTag** da estrutura de valor da propriedade para a propriedade. **** 
  
Se os tipos de propriedade forem especificados no **SPropTagArray** no _lpPropTagArray_, os valores de propriedade no **SPropValue** retornados em _lppPropArray_ têm tipos que correspondem exatamente aos tipos solicitados, a menos que um valor de erro seja retornado nesse. 
  
As propriedades de cadeia de caracteres podem ter um dos dois tipos de propriedade: PT_UNICODE para representar o formato Unicode e PT_STRING8 para representar o formato ANSI. Se o sinalizador MAPI_UNICODE estiver definido no parâmetro _parâmetroulflags_ , sempre que **** GetProps não puder determinar o formato apropriado para uma propriedade de cadeia de caracteres, ele retornará seu valor no formato Unicode. **** GetProps não podem determinar um tipo de propriedade de cadeia de caracteres exata nas seguintes situações: 
  
- O parâmetro _lpPropTagArray_ é definido como nulo para solicitar todas as propriedades. 
    
- O membro **aulPropTag** inclui o valor PT_UNSPECIFIED como seu tipo de propriedade na matriz de marca de propriedade. 
    
Se o parâmetro _lpPropTagArray_ estiver definido como nulo para recuperar todas as propriedades do objeto e nenhuma propriedade existir, GetProps fará o seguinte: **** 
  
- Retorna S_OK.
    
- Define o valor da contagem no membro **cValues** da estrutura de valor da propriedade como 0. 
    
- Define o conteúdo de _lpcValues_ como 0. 
    
- Define _lppPropArray_ como nulo. 
    
 **** GetProps não devem retornar propriedades de vários valores com **cValues** definido como 0. 
  
## <a name="notes-to-implementers"></a>Observações para implementadores

Chame a função [MAPIAllocateBuffer](mapiallocatebuffer.md) para alocar a memória inicialmente para a estrutura [SPropValue](spropvalue.md) indicada por _lpPropTagArray_; Chame [MAPIAllocateMore](mapiallocatemore.md) para alocar qualquer memória adicional necessária para os membros da estrutura. 
  
Retornar MAPI_W_ERRORS_RETURNED se você não puder recuperar o valor de uma ou mais das propriedades solicitadas. Na estrutura de valor da propriedade, defina o tipo no membro **aulPropTag** como PT_ERROR e o membro de **valor** para um código de status que descreva o erro. Por exemplo, se você tiver que converter uma cadeia de caracteres em Unicode e não oferecer suporte a Unicode, defina o **valor** member como MAPI_E_BAD_CHARWIDTH. Se a propriedade for muito grande, defina-a como MAPI_E_NOT_ENOUGH_MEMORY. Se o objeto não oferecer suporte à propriedade, defina-o como MAPI_E_NOT_FOUND. 
  
A implementação de um provedor de transporte remoto **** do método GetProps deve retornar os valores de propriedade da pasta para as propriedades solicitadas pelo chamador. A implementação deve fazer o seguinte: 
  
- Alocar uma matriz de valor de propriedade para retornar ao chamador e armazenar seu endereço no parâmetro de ponteiro de valor de propriedade passado para essa finalidade.
    
- Copie as marcas de propriedade das propriedades da pasta para as marcas de propriedade na matriz de valor de propriedade de acordo com a matriz de marcas **** de propriedade passadas para GetProps.
    
- Certifique-se de que o tipo de propriedade é definido para todas **** as marcas de propriedade passadas para GetProps. O chamador pode passar um tipo de propriedade de PT_UNSPECIFIED, caso em que **** GetProps deve definir o tipo de propriedade correto para essa marca de propriedade. 
    
- Definir o valor de cada propriedade na matriz de valor da propriedade de acordo com sua marca. Por exemplo, se a marca de propriedade solicitada pelo chamador for **PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md)) **** , GetProps poderá definir o valor como MAPI_FOLDER. 
    
- Se o chamador passar em qualquer marca de propriedade que sua implementação não manipula, você pode definir a marca de propriedade para PT_ERROR para essas propriedades e definir o valor da propriedade como MAPI_E_NOT_FOUND.
    
- ReTorne S_OK se nenhum erro ocorreu ou MAPI_W_ERRORS_RETURNED se houvesse erros.
    
A implementação de um provedor de transporte remoto **** do método GetProps deve suportar as seguintes propriedades no mínimo: 
  
- **PR_ACCESS** ([PidTagAccess](pidtagaccess-canonical-property.md))
    
- **PR_ACCESS_LEVEL** ([PidTagAccessLevel](pidtagaccesslevel-canonical-property.md))
    
- **PR_ASSOC_CONTENT_COUNT** ([PidTagAssociatedContentCount](pidtagassociatedcontentcount-canonical-property.md))
    
- **PR_CONTENT_COUNT** ([PidTagContentCount](pidtagcontentcount-canonical-property.md))
    
- **PR_CREATION_TIME** ([PidTagCreationTime](pidtagcreationtime-canonical-property.md))
    
- **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))
    
- **PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md))
    
- **PR_FOLDER_TYPE** ([PidTagFolderType](pidtagfoldertype-canonical-property.md))
    
- **PR_OBJECT_TYPE**
    
- **PR_SUBFOLDERS** ([PidTagSubfolders](pidtagsubfolders-canonical-property.md))
    
## <a name="notes-to-callers"></a>Notas para chamadores

Para propriedades do tipo PT_OBJECT, chame o método [IMAPIProp:: OpenProperty](imapiprop-openproperty.md) em vez de GetProps. **** 
  
Para propriedades seguras, não espere recuperá-las chamando getProps com o parâmetro _lppPropTagArray_ definido como nulo. **** Você deve definir explicitamente um identificador de propriedade segura no membro **aulPropTag** de sua matriz de marca de propriedade quando chamar **** GetProps. Quando e como uma propriedade segura está disponível, o provedor de serviços. 
  
Libere a estrutura **SPropValue** retornada chamando a função [MAPIFreeBuffer](mapifreebuffer.md) somente se GetProps retornar S_OK ou MAPI_W_ERRORS_RETURNED. **** 
  
Se **** GetProps retornar MAPI_W_ERRORS_RETURNED porque ele não pôde acessar uma ou mais propriedades, verifique as marcas de propriedade das propriedades retornadas. As propriedades com falha terão os seguintes valores definidos na estrutura de valor da propriedade: 
  
- O tipo de propriedade no membro **aulPropTag** definido como PT_ERROR. 
    
- O valor da propriedade no membro **Value** definido como um código de status para o erro, como MAPI_E_NOT_FOUND. 
    
As propriedades que falham porque são muito grandes para serem retornadas convenientemente na estrutura de valor da propriedade têm seus membros **Value** definidos como MAPI_E_NOT_ENOUGH_MEMORY. Normalmente, isso ocorre com propriedades binárias ou cadeias de caracteres do tipo PT_STRING8, PT_UNICODE ou PT_BINARY quando o valor da propriedade é 4 KB ou maior. Chame **IMAPIProp:: OpenProperty** para recuperar propriedades grandes. 
  
Nem todas as implementações de getProps oferecem suporte aos formatos Unicode e ANSI para cadeias de caracteres. **** Quando uma propriedade específica requer conversão de formato de **** cadeia de caracteres e GetProps não dão suporte a ela, o membro de **valor** para a propriedade é definido como MAPI_E_BAD_CHARWIDTH. 
  
Para verificar se um PST é um PST do SharePoint, monte o PST usando [IMAPISession:: OpenMsgStore](imapisession-openmsgstore.md)e, **** em seguida, chame GetProps no objeto Message Store solicitando essa propriedade. Se ele existir, você poderá supor que o PST tenha sido configurado para o SharePoint; caso contrário, o PST não foi configurado como um PST do SharePoint. 
  
Para obter mais informações sobre como usar **** GetProps para acessar propriedades, consulte [Retrieving MAPI Properties](retrieving-mapi-properties.md).
  
## <a name="mfcmapi-reference"></a>Referência do MFCMAPI

Para ver códigos de exemplo do MFCMAPI, confira a tabela a seguir.
  
|**Arquivo**|**Função**|**Comentário**|
|:-----|:-----|:-----|
|MAPIFunctions. cpp  <br/> |GetPropsNULL  <br/> |MFCMAPI usa o método **IMAPIProp::** GetProps para obter todas as propriedades de um objeto passando NULL ou a matriz retornada pelo método [IMAPIProp::](imapiprop-getproplist.md) getproplist no parâmetro _lpPropTagArray_ .  <br/> |
   
## <a name="see-also"></a>Confira também



[IMAPIProp::GetPropList](imapiprop-getproplist.md)
  
[IMAPIProp::OpenProperty](imapiprop-openproperty.md)
  
[MAPIAllocateBuffer](mapiallocatebuffer.md)
  
[MAPIAllocateMore](mapiallocatemore.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[SPropTagArray](sproptagarray.md)
  
[SPropValue](spropvalue.md)
  
[IMAPIProp : IUnknown](imapipropiunknown.md)


[MFCMAPI como exemplo de código](mfcmapi-as-a-code-sample.md)
  
[Recuperando propriedades MAPI](retrieving-mapi-properties.md)
  
[Usando macros para tratamento de erros](using-macros-for-error-handling.md)

