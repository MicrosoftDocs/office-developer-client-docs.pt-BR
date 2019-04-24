---
title: IMAPIPropGetNamesFromIDs
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIProp.GetNamesFromIDs
api_type:
- COM
ms.assetid: 3efa4731-cf32-4a6c-9ba8-d059e58b0d98
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: f6688afde9b36a7722eaaf768f091481c15b7308
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32329054"
---
# <a name="imapipropgetnamesfromids"></a>IMAPIProp::GetNamesFromIDs

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Fornece os nomes de propriedade que correspondem a um ou mais identificadores de propriedade.
  
```cpp
HRESULT GetNamesFromIDs(
  LPSPropTagArray FAR * lppPropTags,
  LPGUID lpPropSetGuid,
  ULONG ulFlags,
  ULONG FAR * lpcPropNames,
  LPMAPINAMEID FAR * FAR * lpppPropNames
);
```

## <a name="parameters"></a>Parâmetros

 _lppPropTags_
  
> [in, out] Na entrada, um ponteiro para uma estrutura [SPropTagArray](sproptagarray.md) que contém uma matriz de marcas de propriedade; caso contrário, NULL, indicando que todos os nomes devem ser retornados. O membro **cValues** da matriz de marca de propriedade não pode ser 0. Se _lppPropTags_ for um ponteiro válido na entrada, **GetNamesFromIDs** retornará nomes para cada identificador de propriedade incluído na matriz. 
    
 _lpPropSetGuid_
  
> no Um ponteiro para um GUID ou uma estrutura [GUID](guid.md) , que identifica um conjunto de propriedades. O parâmetro _lpPropSetGuid_ pode apontar para um conjunto de propriedades válido ou pode ser nulo. 
    
 _ulFlags_
  
> no Uma bitmask de sinalizadores que indica o tipo de nome a ser retornado. Os seguintes sinalizadores podem ser usados (se ambos os sinalizadores estiverem definidos, nenhum nome será retornado):
    
MAPI_NO_IDS 
  
> As solicitações que apenas os nomes armazenados como cadeias de caracteres Unicode serão retornadas. 
    
MAPI_NO_STRINGS 
  
> As solicitações que apenas os nomes armazenados como identificadores numéricos serão retornadas. 
    
 _lpcPropNames_
  
> bota Um ponteiro para uma contagem dos ponteiros de nome da propriedade na matriz apontada pelo parâmetro _lppPropNames_ . 
    
 _lpppPropNames_
  
> bota Um ponteiro para uma matriz de ponteiros para estruturas [MAPINAMEID](mapinameid.md) que contêm nomes de propriedade. 
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> Os nomes das propriedades foram retornados com êxito. 
    
MAPI_E_NO_SUPPORT 
  
> O objeto não dá suporte a propriedades nomeadas. 
    
MAPI_W_ERRORS_RETURNED 
  
> A chamada foi concluída com êxito, mas não foi possível retornar os nomes de uma ou mais propriedades. As marcas de propriedade para as propriedades com falha têm um tipo de propriedade de **PT_ERROR**. Quando esse aviso é retornado, a chamada deve ser tratada como bem-sucedida. Para testar esse aviso, use a macro **HR_FAILED** . Para obter mais informações, consulte [usando macros para tratamento de erros](using-macros-for-error-handling.md). 
    
MAPI_E_INVALID_PARAMETER 
  
> O membro **cValues** de uma ou mais das entradas na matriz de marca de propriedade apontada por _lppPropTags_ está definida como 0. 
    
## <a name="remarks"></a>Comentários

Embora o acesso à maioria das propriedades seja pelo identificador de propriedade, algumas propriedades podem ser acessadas pelo nome. O método **IMAPIProp:: GetNamesFromIDs** pode ser chamado para fazer o seguinte: 
  
- Recuperar nomes de identificadores de propriedade específicos em um conjunto específico de propriedades.
    
- Recupere nomes para identificadores de propriedade específicos em qualquer conjunto de propriedades.
    
- Recuperar nomes de todas as propriedades nomeadas incluídas no mapeamento do objeto.
    
Se _lppPropTags_ apontar para uma matriz de marca de propriedade válida com um ou mais identificadores de propriedade e _lpPropSetGuid_ apontar para um conjunto de propriedades válido, **GetNamesFromIDs** ignorará o conjunto de propriedades e os tipos de propriedade e retornará todos os nomes que mapeiam para os identificadores especificados. 
  
Se _lppPropTags_ apontar para uma matriz de marca de propriedade válida com um ou mais identificadores de propriedade e _lpPropSetGuid_ for nulo, **GetNamesFromIDs** retornará todos os nomes que mapeiam para os identificadores especificados. 
  
Se um identificador especificado não tiver um nome, **GetNamesFromIDs** retornará NULL no local desse identificador na estrutura retornada no _lpppPropNames_ e também retornará MAPI_W_ERRORS_RETURNED. 
  
Se _lpPropSetGuid_ e _lppPropTags_ forem nulos, **GetNamesFromIDs** aloca uma nova matriz de marca de propriedade e retorna todos os nomes de todas as propriedades nomeadas para o objeto. 
  
Quando não há nomes a serem retornados, talvez porque não há propriedades no conjunto de propriedades solicitadas ou todas as propriedades são de um tipo excluído pelos sinalizadores, **GetNamesFromIDs** faz o seguinte: 
  
- Retorna S_OK.
    
- Aloca uma nova estrutura **SPropTagArray** , definindo o membro **cValues** como 0. 
    
- Define o conteúdo de _lpcPropNames_ como 0. 
    
- Define o conteúdo de _lpppPropNames_ como nulo. 
    
## <a name="notes-to-implementers"></a>Observações para implementadores

Se _lpPropSetGuid_ apontar para um conjunto de propriedades válido e _lppPropTags_ for nulo, o resultado será indefinido. Você pode usar uma das seguintes estratégias: 
  
- Ignore o conjunto de propriedades e retorne os nomes dos identificadores na matriz de marca de propriedade.
    
- ReTorne os nomes somente para os identificadores na matriz de marca de propriedade que pertencem ao conjunto de propriedades especificado.
    
- Falha na chamada, retornando MAPI_E_INVALID_PARAMETER. 
    
## <a name="notes-to-callers"></a>Notas para chamadores

Para recuperar todas as propriedades nomeadas de um objeto, primeiro você deve chamar o método [IMAPIProp::](imapiprop-getproplist.md) getproplist do objeto e, em seguida, passar os identificadores retornados que estão acima do intervalo da 0X8000 para **GetNamesFromIDs**.
  
Se você passar um conjunto de propriedades válido, mas não uma matriz de marca de propriedade válida, esteja preparado para resultados imprevisíveis. Algumas implementações de **GetNamesFromIDs** ignoram o conjunto de propriedades e retornam os nomes dos identificadores na matriz de marca de propriedade. Algumas implementações retornam MAPI_E_INVALID_PARAMETER. Ainda outras implementações retornam nomes para identificadores de todas as propriedades no conjunto de propriedades. Se o conjunto de Propriedades for PS_PUBLIC_STRINGS, **GetNamesFromIDs** poderá retornar todos os nomes que já foram criados. Se o provedor de serviços armazena uma propriedade sob os identificadores associados com as cadeias de caracteres públicas é irrelevante. 
  
Quando você tiver concluído os nomes das propriedades, verifique o conteúdo do parâmetro _lpcPropNames_ para determinar se algum nome foi retornado. Em caso afirmativo, chame a função [MAPIFreeBuffer](mapifreebuffer.md) para liberar a memória indicada por _lppPropTags_ e _lpppPropNames_ quando um resultado bem-sucedido é retornado. Uma chamada para **MAPIFreeBuffer** é suficiente para cada parâmetro; Você não precisa atravessar a matriz de ponteiros e liberar cada estrutura **MAPINAMEID** individualmente. 
  
Para obter mais informações sobre propriedades nomeadas, consulte [MAPI Named Properties](mapi-named-properties.md). 
  
## <a name="mfcmapi-reference"></a>Referência do MFCMAPI

Para ver códigos de exemplo do MFCMAPI, confira a tabela a seguir.
  
|**Arquivo**|**Função**|**Comentário**|
|:-----|:-----|:-----|
|SingleMAPIPropListCtrl. cpp  <br/> |CSingleMAPIPropListCtrl:: FindAllNamedProps  <br/> |MFCMAPI usa o método **IMAPIProp:: GetNamesFromIDs** para pesquisar propriedades nomeadas que foram mapeadas anteriormente.  <br/> |
   
## <a name="see-also"></a>Confira também



[GUID](guid.md)
  
[IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md)
  
[IMAPIProp::GetPropList](imapiprop-getproplist.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[MAPINAMEID](mapinameid.md)
  
[SPropTagArray](sproptagarray.md)
  
[IMAPIProp : IUnknown](imapipropiunknown.md)


[MFCMAPI como exemplo de código](mfcmapi-as-a-code-sample.md)
  
[MAPI denominada propriedades](mapi-named-properties.md)
  
[Usando macros para tratamento de erros](using-macros-for-error-handling.md)

