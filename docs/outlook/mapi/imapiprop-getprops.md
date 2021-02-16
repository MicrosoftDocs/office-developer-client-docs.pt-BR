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
  
> [in] Um ponteiro para uma matriz de marcas de propriedade que identificam as propriedades cujos valores devem ser recuperados. O  _parâmetro lpPropTagArray_ deve ser NULL, indicando que os valores de todas as propriedades do objeto devem ser retornados ou apontar para uma estrutura [SPropTagArray](sproptagarray.md) que contém uma ou mais marcas de propriedade. 
    
 _ulFlags_
  
> [in] Uma máscara de bits de sinalizadores que indica o formato das propriedades que têm o tipo PT_UNSPECIFIED. O sinalizador a seguir pode ser definido:
    
MAPI_UNICODE 
  
> Os valores de cadeia de caracteres dessas propriedades devem ser retornados no formato Unicode. Se o MAPI_UNICODE não estiver definido, os valores da cadeia de caracteres deverão ser retornados no formato ANSI.
    
 _lpcValues_
  
> [out] Um ponteiro para uma contagem de valores de propriedade apontados pelo _parâmetro lppPropArray._ Se  _lppPropArray_ for NULL, o conteúdo do parâmetro  _lpcValues_ será zero. 
    
 _lppPropArray_
  
> [out] Um ponteiro para um ponteiro para os valores de propriedade recuperados.
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> Os valores da propriedade foram recuperados com êxito.
    
MAPI_W_ERRORS_RETURNED 
  
> A chamada foi bem-sucedida em geral, mas uma ou mais propriedades não puderam ser acessadas. O **membro aulPropTag** do valor da propriedade para cada propriedade indisponível tem um tipo de PT_ERROR e um identificador zero. Quando esse aviso é retornado, a chamada deve ser tratada como bem-sucedida. Para testar esse aviso, use a **HR_FAILED** macro. Para obter mais informações, consulte [Usando macros para tratamento de erros.](using-macros-for-error-handling.md)
    
MAPI_E_INVALID_PARAMETER 
  
> Zero foi passado no **membro cValues** da **estrutura SPropTagArray** apontado por  _lpPropTagArray_.
    
## <a name="remarks"></a>Comentários

O **método IMAPIProp::GetProps** obtém os valores de propriedade de uma ou mais propriedades de um objeto. 
  
Os valores de propriedade são retornados na mesma ordem em que foram solicitados (ou seja, a ordem das propriedades na matriz de marca de propriedade apontada por  _lpPropTagArray_ corresponde à ordem na matriz de estruturas de valores de propriedade apontadas por  _lppPropArray_). 
  
Os tipos de propriedade especificados nos membros **aulPropTag** da matriz de marca de propriedade indicam o tipo de valor que deve ser retornado no membro **Value** de cada estrutura de valores de propriedade. No entanto, se o chamador não sabe o tipo de uma propriedade, o tipo no membro **aulPropTag** pode ser definido como PT_UNSPECIFIED. Ao recuperar o valor, **GetProps** define o tipo correto no membro **aulPropTag** da estrutura de valores da propriedade para a propriedade. 
  
Se os tipos de propriedade são especificados em **SPropTagArray** em  _lpPropTagArray_, os valores de propriedade em **SPropValue** retornados em  _lppPropArray_ têm tipos que exatamente corresponder aos tipos solicitados, a menos que um valor de erro seja retornado em vez disso. 
  
Propriedades de cadeia de caracteres podem ter um de dois tipos de propriedade: PT_UNICODE para representar o formato Unicode e PT_STRING8 para representar o formato ANSI. Se o sinalizador MAPI_UNICODE for definido no parâmetro  _ulFlags,_ sempre que **GetProps** não puder determinar o formato apropriado para uma propriedade de cadeia de caracteres, ele retornará seu valor no formato Unicode. **GetProps** não pode determinar um tipo de propriedade de cadeia de caracteres exata nas seguintes situações: 
  
- O  _parâmetro lpPropTagArray_ é definido como NULL para solicitar todas as propriedades. 
    
- O **membro aulPropTag** inclui o valor PT_UNSPECIFIED como seu tipo de propriedade na matriz de marca de propriedade. 
    
Se o  _parâmetro lpPropTagArray_ for definido como NULL para recuperar todas as propriedades do objeto e nenhuma propriedade existir, **GetProps** faz o seguinte: 
  
- Retorna S_OK.
    
- Define o valor de contagem no **membro cValues** da estrutura de valores da propriedade como 0. 
    
- Define o conteúdo de  _lpcValues_ como 0. 
    
- Define  _lppPropArray_ como NULL. 
    
 **GetProps** não deve retornar propriedades de vários valores com **cValues** definido como 0. 
  
## <a name="notes-to-implementers"></a>Observações para implementadores

Chame a [função MAPIAllocateBuffer](mapiallocatebuffer.md) para alocar memória inicialmente para a estrutura [SPropValue](spropvalue.md) apontada por  _lpPropTagArray_; chame [MAPIAllocateMore](mapiallocatemore.md) para alocar qualquer memória adicional necessária para os membros da estrutura. 
  
Retorne MAPI_W_ERRORS_RETURNED se não for possível recuperar o valor de uma ou mais das propriedades solicitadas. Na estrutura de valores de propriedade, de definir o tipo no membro **aulPropTag** como PT_ERROR e o membro **Value** como um código de status que descreve o erro. Por exemplo, se você tiver que converter uma cadeia de caracteres em Unicode e não suportar Unicode, de definir o membro **Value** como MAPI_E_BAD_CHARWIDTH. Se a propriedade for muito grande, de definida como MAPI_E_NOT_ENOUGH_MEMORY. Se o objeto não suportar a propriedade, de definida como MAPI_E_NOT_FOUND. 
  
A implementação do método **GetProps** de um provedor de transporte remoto deve retornar os valores de propriedade da pasta para as propriedades solicitadas pelo chamador. Sua implementação deve fazer o seguinte: 
  
- Aloce uma matriz de valores de propriedade para retornar ao chamador e armazenar seu endereço no parâmetro de ponteiro de valor de propriedade passado para essa finalidade.
    
- Copie as marcas de propriedade das propriedades da pasta para as marcas de propriedade na matriz de valores de propriedade de acordo com a matriz de marcas de propriedade passadas para **GetProps**.
    
- Certifique-se de que o tipo de propriedade está definido para todas as marcas de propriedade **passadas para GetProps**. O chamador pode passar um tipo de propriedade PT_UNSPECIFIED, nesse **caso, GetProps** deve definir o tipo de propriedade correto para essa marca de propriedade. 
    
- Definir o valor de cada propriedade na matriz de valores de propriedade de acordo com sua marca. Por exemplo, se a marca de propriedade solicitada pelo chamador for **PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md)), **GetProps** poderá definir o valor como MAPI_FOLDER. 
    
- Se o chamador passar qualquer marca de propriedade que sua implementação não manipular, você poderá definir a marca de propriedade como PT_ERROR para essas propriedades e definir o valor da propriedade como MAPI_E_NOT_FOUND.
    
- Retorne S_OK se não houver erros ou MAPI_W_ERRORS_RETURNED se houver erros.
    
A implementação do método **GetProps** de um provedor de transporte remoto deve dar suporte mínimo às seguintes propriedades: 
  
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

Para propriedades do tipo PT_OBJECT, chame o método [IMAPIProp::OpenProperty](imapiprop-openproperty.md) em vez de **GetProps**. 
  
Para propriedades seguras, não espere recuperá-las chamando **GetProps** com o parâmetro  _lppPropTagArray_ definido como NULL. Você deve definir explicitamente o identificador de uma propriedade segura no membro **aulPropTag** de sua matriz de marca de propriedade ao chamar **GetProps**. Quando e como uma propriedade segura está disponível fica para o provedor de serviços. 
  
Liberar a estrutura **SPropValue** retornada chamando a função [MAPIFreeBuffer](mapifreebuffer.md) somente se **GetProps** retornar S_OK ou MAPI_W_ERRORS_RETURNED. 
  
Se **GetProps** retornar MAPI_W_ERRORS_RETURNED porque não pôde acessar uma ou mais propriedades, verifique as marcas de propriedade das propriedades retornadas. As propriedades com falha terão os seguintes valores definidos em sua estrutura de valores de propriedade: 
  
- O tipo de propriedade no **membro aulPropTag** definido como PT_ERROR. 
    
- O valor da propriedade no **membro Value** definido como um código de status para o erro, como MAPI_E_NOT_FOUND. 
    
As propriedades que falham porque são muito grandes para serem convenientemente retornadas na estrutura de valores da propriedade têm seu membro **Value** definido como MAPI_E_NOT_ENOUGH_MEMORY. Normalmente, isso ocorre com propriedades de cadeia de caracteres ou binárias do tipo PT_STRING8, PT_UNICODE ou PT_BINARY quando o valor da propriedade é 4 KB ou maior. Chame **IMAPIProp::OpenProperty** para recuperar propriedades grandes. 
  
Nem todas as implementações de **GetProps** suportam os formatos Unicode e ANSI para cadeias de caracteres. Quando uma propriedade específica requer conversão de formato de cadeia de caracteres e **GetProps** não pode dar suporte a ela, o membro **Value** da propriedade é definido como MAPI_E_BAD_CHARWIDTH. 
  
Para verificar se um PST é um PST do SharePoint, monte o PST usando [IMAPISession::OpenMsgStore](imapisession-openmsgstore.md), em seguida, chame **GetProps** no objeto do repositório de mensagens solicitando essa propriedade. Se existir, você pode presumir que o PST foi configurado para o SharePoint; caso não tenha sido, o PST não foi configurado como um PST do SharePoint. 
  
Para obter mais informações sobre como usar **GetProps** para acessar propriedades, consulte [Recuperando propriedades MAPI](retrieving-mapi-properties.md).
  
## <a name="mfcmapi-reference"></a>Referência do MFCMAPI

Para ver códigos de exemplo do MFCMAPI, confira a tabela a seguir.
  
|**Arquivo**|**Função**|**Comentário**|
|:-----|:-----|:-----|
|MAPIFunctions.cpp  <br/> |GetPropsNULL  <br/> |MFCMAPI usa o método **IMAPIProp::GetProps** para obter todas as propriedades de um objeto passando NULL ou a matriz retornada pelo método [IMAPIProp::GetPropList](imapiprop-getproplist.md) no parâmetro _lpPropTagArray._  <br/> |
   
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
  
[Recuperar propriedades MAPI](retrieving-mapi-properties.md)
  
[Usando macros para tratamento de erros](using-macros-for-error-handling.md)

