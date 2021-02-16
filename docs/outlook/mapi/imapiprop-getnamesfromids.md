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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33423570"
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
  
> [in, out] Na entrada, um ponteiro para uma [estrutura SPropTagArray](sproptagarray.md) que contém uma matriz de marcas de propriedade; caso contrário, NULL, indicando que todos os nomes devem ser retornados. O **membro cValues** da matriz de marca de propriedade não pode ser 0. Se  _lppPropTags_ for um ponteiro válido na entrada, **GetNamesFromIDs** retornará nomes para cada identificador de propriedade incluído na matriz. 
    
 _lpPropSetGuid_
  
> [in] Um ponteiro para um GUID ou uma [estrutura GUID](guid.md) que identifica um conjunto de propriedades. O  _parâmetro lpPropSetGuid_ pode apontar para um conjunto de propriedades válido ou pode ser NULL. 
    
 _ulFlags_
  
> [in] Uma máscara de bits de sinalizadores que indica o tipo de nomes a serem retornados. Os sinalizadores a seguir podem ser usados (se ambos os sinalizadores estão definidos, nenhum nome será retornado):
    
MAPI_NO_IDS 
  
> Solicita que apenas nomes armazenados como cadeias de caracteres Unicode sejam retornados. 
    
MAPI_NO_STRINGS 
  
> Solicita que apenas nomes armazenados como identificadores numéricos sejam retornados. 
    
 _lpcPropNames_
  
> [out] Um ponteiro para uma contagem dos ponteiros do nome da propriedade na matriz apontada pelo _parâmetro lppPropNames._ 
    
 _lpppPropNames_
  
> [out] Um ponteiro para uma matriz de ponteiros para estruturas [MAPINAMEID](mapinameid.md) que contém nomes de propriedade. 
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> Os nomes das propriedades foram retornados com êxito. 
    
MAPI_E_NO_SUPPORT 
  
> O objeto não dá suporte a propriedades nomeadas. 
    
MAPI_W_ERRORS_RETURNED 
  
> A chamada foi bem-sucedida em geral, mas não foi possível retornar nomes para uma ou mais propriedades. As marcas de propriedade para as propriedades com falha têm um tipo de propriedade **PT_ERROR**. Quando esse aviso é retornado, a chamada deve ser tratada como bem-sucedida. Para testar esse aviso, use a **HR_FAILED** macro. Para obter mais informações, consulte [Usando macros para tratamento de erros.](using-macros-for-error-handling.md) 
    
MAPI_E_INVALID_PARAMETER 
  
> O **membro cValues** de uma ou mais entradas na matriz de marca de propriedade apontado por  _lppPropTags_ é definido como 0. 
    
## <a name="remarks"></a>Comentários

Embora o acesso à maioria das propriedades seja por identificador de propriedade, algumas propriedades podem ser acessadas por nome. O **método IMAPIProp::GetNamesFromIDs** pode ser chamado para fazer o seguinte: 
  
- Recuperar nomes para identificadores de propriedade específicos em um conjunto de propriedades específico.
    
- Recuperar nomes para identificadores de propriedade específicos em qualquer conjunto de propriedades.
    
- Recupere nomes para todas as propriedades nomeadas incluídas no mapeamento do objeto.
    
Se  _lppPropTags_ aponta para uma matriz de marcas de propriedade válida com um ou mais identificadores de propriedade e  _lpPropSetGuid_ aponta para um conjunto de propriedades válido, **GetNamesFromIDs** ignora o conjunto de propriedades e os tipos de propriedade e retorna todos os nomes mapeados para os identificadores especificados. 
  
Se  _lppPropTags_ aponta para uma matriz de marcas de propriedade válida com um ou mais identificadores de propriedade e  _lpPropSetGuid_ é NULL, **GetNamesFromIDs** retorna todos os nomes mapeados para os identificadores especificados. 
  
Se um identificador especificado não tiver um nome, **GetNamesFromIDs** retornará NULL no lugar desse identificador na estrutura retornada em  _lpppPropNames_ e também retornará MAPI_W_ERRORS_RETURNED. 
  
Se  _lpPropSetGuid_ e  _lppPropTags_ são NULL, **GetNamesFromIDs** aloca uma nova matriz de marcas de propriedade e retorna todos os nomes para todas as propriedades nomeadas para o objeto. 
  
Quando não há nomes a serem retornados, talvez porque não haja propriedades no conjunto de propriedades solicitado ou todas as propriedades sejam de um tipo excluído pelos sinalizadores, **GetNamesFromIDs** faz o seguinte: 
  
- Retorna S_OK.
    
- Aloca uma nova **estrutura SPropTagArray,** definindo o **membro cValues** como 0. 
    
- Define o conteúdo de  _lpcPropNames_ como 0. 
    
- Define o conteúdo de  _lpppPropNames_ como NULL. 
    
## <a name="notes-to-implementers"></a>Observações para implementadores

Se  _lpPropSetGuid_ aponta para um conjunto de propriedades válido e  _lppPropTags_ for NULL, o resultado será indefinido. Você pode usar uma das seguintes estratégias: 
  
- Ignore o conjunto de propriedades e retorne os nomes dos identificadores na matriz de marcas de propriedade.
    
- Retorne os nomes apenas para os identificadores na matriz de marcas de propriedade que pertencem ao conjunto de propriedades especificado.
    
- Falha na chamada, retornando MAPI_E_INVALID_PARAMETER. 
    
## <a name="notes-to-callers"></a>Notas para chamadores

Para recuperar todas as propriedades nomeadas para um objeto, primeiro você deve chamar o método [IMAPIProp::GetPropList](imapiprop-getproplist.md) do objeto e, em seguida, passar os identificadores retornados que estão acima do intervalo 0x8000 **para GetNamesFromIDs**.
  
Se você passar um conjunto de propriedades válido, mas não uma matriz de marca de propriedade válida, esteja preparado para resultados imprevisíveis. Algumas implementações de **GetNamesFromIDs** ignoram o conjunto de propriedades e retornam os nomes dos identificadores na matriz de marcas de propriedade. Algumas implementações retornam MAPI_E_INVALID_PARAMETER. Outras implementações ainda retornam nomes para identificadores de todas as propriedades no conjunto de propriedades. Se o conjunto de propriedades PS_PUBLIC_STRINGS, **GetNamesFromIDs** poderá retornar todos os nomes que já foram criados. Se o provedor de serviços armazena uma propriedade sob os identificadores associados às cadeias de caracteres públicas é imaterial. 
  
Quando terminar os nomes de propriedade, verifique o conteúdo do parâmetro  _lpcPropNames_ para determinar se algum nome foi retornado. Em caso afirmativa, chame a função [MAPIFreeBuffer](mapifreebuffer.md) para liberar a memória apontada por  _lppPropTags_ e  _lpppPropNames_ quando um resultado bem-sucedido for retornado. Uma chamada para **MAPIFreeBuffer** é suficiente para cada parâmetro; você não precisa percorrer a matriz de ponteiros e liberar cada **estrutura MAPINAMEID** individualmente. 
  
Para obter mais informações sobre propriedades nomeadas, consulte [MAPI Named Properties](mapi-named-properties.md). 
  
## <a name="mfcmapi-reference"></a>Referência do MFCMAPI

Para ver códigos de exemplo do MFCMAPI, confira a tabela a seguir.
  
|**Arquivo**|**Função**|**Comentário**|
|:-----|:-----|:-----|
|SingleMAPIPropListCtrl.cpp  <br/> |CSingleMAPIPropListCtrl::FindAllNamedProps  <br/> |MFCMAPI usa o **método IMAPIProp::GetNamesFromIDs** para procurar propriedades nomeadas que foram mapeadas anteriormente.  <br/> |
   
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

