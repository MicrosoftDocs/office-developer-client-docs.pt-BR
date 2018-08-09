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
ms.openlocfilehash: 33351235db2a9a3f9d9b67f59e8356a0fa8abfa8
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19767148"
---
# <a name="imapipropgetprops"></a>IMAPIProp::GetProps

  
  
**Aplica-se a**: Outlook 
  
Recupera o valor da propriedade de uma ou mais propriedades de um objeto.
  
```cpp
HRESULT GetProps(
  LPSPropTagArray lpPropTagArray,
  ULONG ulFlags,
  ULONG FAR * lpcValues,
  LPSPropValue FAR * lppPropArray
);
```

## <a name="parameters"></a>Par�metros

 _lpPropTagArray_
  
> [in] Um ponteiro para uma matriz de marcas de propriedade que identificam as propriedades cujos valores devem ser recuperadas. O parâmetro _lpPropTagArray_ deve ser um dos NULL, indicando que valores para todas as propriedades do objeto devem ser retornados ou apontar para uma estrutura [SPropTagArray](sproptagarray.md) que contém uma ou mais marcas de propriedade. 
    
 _ulFlags_
  
> [in] Uma bitmask dos sinalizadores que indica o formato para propriedades que tenham o tipo PT_UNSPECIFIED. O seguinte sinalizador pode ser definido:
    
MAPI_UNICODE 
  
> Os valores de cadeia de caracteres para essas propriedades devem ser retornados no formato Unicode. Se o sinalizador MAPI_UNICODE não estiver definido, os valores de cadeia de caracteres devem ser retornados no formato ANSI.
    
 _lpcValues_
  
> [out] Um ponteiro para uma contagem de valores de propriedade apontado pelo parâmetro _lppPropArray_ . Se _lppPropArray_ for NULL, o conteúdo do parâmetro _lpcValues_ é zero. 
    
 _lppPropArray_
  
> [out] Um ponteiro para um ponteiro para os valores de propriedade recuperadas.
    
## <a name="return-value"></a>Valor retornado

S_OK 
  
> Os valores de propriedade foram recuperados com êxito.
    
MAPI_W_ERRORS_RETURNED 
  
> Chamada bem-sucedida, mas não foi possível acessar uma ou mais propriedades. O membro **aulPropTag** do valor da propriedade para cada propriedade indisponível tem um tipo de propriedade de PT_ERROR e um identificador do zero. Quando esse aviso é retornado, a chamada deve ser manipulada com êxito. Para testar esse aviso, use a macro **HR_FAILED** . Para obter mais informações, consulte [Usando Macros para tratamento de erros](using-macros-for-error-handling.md).
    
MAPI_E_INVALID_PARAMETER 
  
> O membro **cValues** da estrutura **SPropTagArray** apontado pela _lpPropTagArray_foi passado zero.
    
## <a name="remarks"></a>Comentários

O método **IMAPIProp::GetProps** obtém os valores de propriedade de uma ou mais propriedades de um objeto. 
  
Os valores de propriedade são retornados na mesma ordem conforme eles foram solicitados (ou seja, a ordem das propriedades na matriz de marca de propriedade indicada por _lpPropTagArray_ correspondências a ordem na matriz de estruturas de valor de propriedade apontado pela _lppPropArray _). 
  
Os tipos de propriedades especificados na matriz de marca de propriedades membros **aulPropTag** indicam o tipo de valor que deve ser retornada no membro do **valor** de cada estrutura de valor de propriedade. No entanto, se o chamador não souber o tipo de uma propriedade, o tipo no membro **aulPropTag** pode ser definido em vez disso, como PT_UNSPECIFIED. Em recuperar o valor, **GetProps** define o tipo correto no membro **aulPropTag** da estrutura de valor de propriedade para a propriedade. 
  
Se os tipos de propriedade forem especificados no **SPropTagArray** no _lpPropTagArray_, os valores de propriedade em **SPropValue** retornados em _lppPropArray_ possuem tipos que correspondem exatamente os tipos de solicitada, a menos que um valor de erro será retornado em vez disso. 
  
Propriedades de cadeia de caracteres podem ter um dos dois tipos de propriedade: PT_UNICODE para representar o formato Unicode e PT_STRING8 para representar o formato ANSI. Se o sinalizador MAPI_UNICODE é definido no parâmetro _ulFlags_ , sempre que **GetProps** não consegue determinar o formato apropriado para uma propriedade de cadeia de caracteres, ele retorna seu valor no formato Unicode. **GetProps** não pode determinar um tipo de propriedade de cadeia de caracteres exato nas seguintes situações: 
  
- O parâmetro de _lpPropTagArray_ é definido como nulo para solicitar todas as propriedades. 
    
- O membro **aulPropTag** inclui o valor PT_UNSPECIFIED como seu tipo de propriedade da matriz de marca de propriedade. 
    
Se o parâmetro _lpPropTagArray_ é definido como NULL para recuperar todas as propriedades do objeto, e não existem propriedades, **GetProps** faz o seguinte: 
  
- Retorna S_OK.
    
- Define o valor de contagem no membro **cValues** da estrutura de valor da propriedade como 0. 
    
- Define o conteúdo de _lpcValues_ como 0. 
    
- Define _lppPropArray_ como NULL. 
    
 **GetProps** não deve retornar as propriedades de valores múltiplos com **cValues** definido como 0. 
  
## <a name="notes-to-implementers"></a>Notas para implementadores

Chamar a função de [MAPIAllocateBuffer](mapiallocatebuffer.md) para alocar memória inicialmente para a estrutura de [SPropValue](spropvalue.md) apontada pela _lpPropTagArray_; Chame [MAPIAllocateMore](mapiallocatemore.md) para alocar toda a memória adicional necessária para que os membros da estrutura. 
  
Retorne MAPI_W_ERRORS_RETURNED se você não pode recuperar o valor para uma ou mais das propriedades solicitadas. Na estrutura de valor de propriedade, defina o tipo no membro **aulPropTag** a PT_ERROR e o membro de **valor** a um código de status que descreve o erro. Por exemplo, se você tiver que converter uma cadeia de caracteres Unicode e não oferecem suporte a Unicode, defina o **valor** de membro para MAPI_E_BAD_CHARWIDTH. Se a propriedade for muito grande, você deve defini-la como MAPI_E_NOT_ENOUGH_MEMORY. Se o objeto não dá suporte para a propriedade, você deve defini-la como E_NOT_FOUND. 
  
Implementação de um provedor transporte remoto do método **GetProps** deve retornar valores de propriedade da pasta para propriedades solicitadas pelo chamador. A implementação deve fazer o seguinte: 
  
- Aloca uma matriz de valores de propriedade para retornar ao chamador e armazenar o respectivo endereço no parâmetro propriedade valor ponteiro passado para essa finalidade.
    
- Copie as marcas de propriedade de propriedades da pasta para as marcas de propriedade da matriz de valores de propriedade de acordo com a matriz de marcas de propriedade passado para **GetProps**.
    
- Certifique-se de que o tipo de propriedade é definido para todas as marcas de propriedade passadas para **GetProps**. O chamador pode passar em um tipo de propriedade de PT_UNSPECIFIED, nesse caso **GetProps** deve definir o tipo de propriedade correta para essa marca de propriedade. 
    
- Defina o valor de cada propriedade da matriz de valores de propriedade de acordo com a sua marca. Por exemplo, se a marca de propriedade solicitada pelo chamador for **PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md)), **GetProps** pode definir o valor para MAPI_FOLDER. 
    
- Se o chamador passa em quaisquer marcas de propriedade não processa a implementação, você pode definir a marca de propriedade para PT_ERROR para essas propriedades e defina o valor da propriedade como E_NOT_FOUND.
    
- Retorno MAPI_W_ERRORS_RETURNED se houver erros ou S_OK se nenhum erro ocorreu.
    
Implementação de um provedor transporte remoto do método **GetProps** deve suportar as seguintes propriedades no mínimo: 
  
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

Para propriedades do tipo PT_OBJECT, chame o método de [IMAPIProp::OpenProperty](imapiprop-openproperty.md) em vez de **GetProps**. 
  
Para propriedades seguras, não espera recuperá-las chamando **GetProps** com o parâmetro _lppPropTagArray_ definido como NULL. Você deve definir explicitamente o identificador de uma propriedade seguro no membro **aulPropTag** da sua matriz de marca de propriedade quando você chama **GetProps**. Quando e como uma propriedade segura está disponível é o provedor de serviços. 
  
Libere a estrutura de **SPropValue** retornada chamando-se a função [MAPIFreeBuffer](mapifreebuffer.md) somente se **GetProps** Retorna S_OK ou MAPI_W_ERRORS_RETURNED. 
  
Se **GetProps** retornar MAPI_W_ERRORS_RETURNED porque não foi possível acessar uma ou mais propriedades, verifique as marcas de propriedade das propriedades retornadas. As propriedades com falha terá definidos na sua estrutura de valor de propriedade de valores a seguir: 
  
- O tipo de propriedade no membro **aulPropTag** definido como PT_ERROR. 
    
- O valor da propriedade no membro do **valor** definido como um código de status para o erro, como E_NOT_FOUND. 
    
Propriedades que falham porque eles são muito grandes para ser retornado convenientemente na estrutura do valor da propriedade têm sua membro de **valor** definido como MAPI_E_NOT_ENOUGH_MEMORY. Geralmente, isso ocorre com propriedades de cadeia de caracteres ou binário do tipo PT_STRING8, PT_UNICODE ou PT_BINARY quando o valor da propriedade é 4 KB ou maior. Chame **IMAPIProp::OpenProperty** para recuperar as propriedades grandes. 
  
Nem todas as implementações de **GetProps** oferecem suporte a formatos ANSI e Unicode para cadeias de caracteres. Quando uma determinada propriedade requer a conversão de formato de cadeia de caracteres e **GetProps** não oferece suporte a ele, o membro de **valor** da propriedade é definido como MAPI_E_BAD_CHARWIDTH. 
  
Para verificar se um PST é um PST do SharePoint, monte o PST usando [IMAPISession::OpenMsgStore](imapisession-openmsgstore.md), ligar **GetProps** no objeto de repositório de mensagem solicitando a essa propriedade. Se ele existir, você pode assumir que o PST foi configurado para o SharePoint; Caso contrário, o PST não tenha sido configurado como um PST do SharePoint. 
  
Para obter mais informações sobre como usar o **GetProps** para acessar as propriedades, consulte [Recuperando propriedades de MAPI](retrieving-mapi-properties.md).
  
## <a name="mfcmapi-reference"></a>Referência MFCMAPI

Para exemplos de código MFCMAPI, consulte a tabela a seguir.
  
|**Arquivo**|**Function**|**Comment**|
|:-----|:-----|:-----|
|MAPIFunctions.cpp  <br/> |GetPropsNULL  <br/> |MFCMAPI usa o método **IMAPIProp::GetProps** para obter todas as propriedades de um objeto passando a matriz retornada pelo método [IMAPIProp::GetPropList](imapiprop-getproplist.md) no parâmetro _lpPropTagArray_ ou nulo.  <br/> |
   
## <a name="see-also"></a>Confira também



[IMAPIProp::GetPropList](imapiprop-getproplist.md)
  
[IMAPIProp::OpenProperty](imapiprop-openproperty.md)
  
[MAPIAllocateBuffer](mapiallocatebuffer.md)
  
[MAPIAllocateMore](mapiallocatemore.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[SPropTagArray](sproptagarray.md)
  
[SPropValue](spropvalue.md)
  
[IMAPIProp : IUnknown](imapipropiunknown.md)


[MFCMAPI como um exemplo de código](mfcmapi-as-a-code-sample.md)
  
[Recuperar as propriedades MAPI](retrieving-mapi-properties.md)
  
[Usar macros para lidar com erros](using-macros-for-error-handling.md)

