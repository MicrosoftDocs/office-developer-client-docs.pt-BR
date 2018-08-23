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
ms.openlocfilehash: 186afd6a80d0ae3ae0a767456e60b2ebaaa579b9
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22574381"
---
# <a name="imapipropgetnamesfromids"></a>IMAPIProp::GetNamesFromIDs

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Fornece os nomes de propriedades que correspondem a um ou mais identificadores de propriedade.
  
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
  
> [além, out] Na entrada, um ponteiro para uma estrutura [SPropTagArray](sproptagarray.md) que contém uma matriz de marcas de propriedade; Caso contrário, NULL, indicando que todos os nomes devem ser retornados. O membro **cValues** para a matriz de marca de propriedade não pode ser 0. Se _lppPropTags_ for um ponteiro válido na entrada, **GetNamesFromIDs** retorna os nomes de cada identificador de propriedade incluídos na matriz. 
    
 _lpPropSetGuid_
  
> [in] Um ponteiro para um GUID ou um [GUID](guid.md) estrutura, que identifica um conjunto de propriedades. O parâmetro _lpPropSetGuid_ pode apontar para um conjunto de propriedades válido ou pode ser NULL. 
    
 _ulFlags_
  
> [in] Uma bitmask dos sinalizadores que indica o tipo de nomes a serem retornadas. Sinalizadores a seguir podem ser usados (se ambos os sinalizadores estão definidos, sem nomes serão retornados):
    
MAPI_NO_IDS 
  
> Solicitações que somente os nomes armazenados como cadeias de caracteres Unicode ser retornado. 
    
MAPI_NO_STRINGS 
  
> Solicitações que somente os nomes armazenados como identificadores numéricos ser retornado. 
    
 _lpcPropNames_
  
> [out] Um ponteiro para uma contagem dos ponteiros de nome de propriedade na matriz apontado pelo parâmetro _lppPropNames_ . 
    
 _lpppPropNames_
  
> [out] Um ponteiro para uma matriz de ponteiros para estruturas [MAPINAMEID](mapinameid.md) que contém os nomes de propriedade. 
    
## <a name="return-value"></a>Valor retornado

S_OK 
  
> Os nomes de propriedade foram retornados com êxito. 
    
MAPI_E_NO_SUPPORT 
  
> O objeto não dá suporte a propriedades nomeadas. 
    
MAPI_W_ERRORS_RETURNED 
  
> Chamada bem-sucedida, mas os nomes para uma ou mais propriedades não puderam ser retornados. As marcas de propriedade para as propriedades de falha têm um tipo de propriedade de **PT_ERROR**. Quando esse aviso é retornado, a chamada deve ser manipulada com êxito. Para testar esse aviso, use a macro **HR_FAILED** . Para obter mais informações, consulte [Usando Macros para tratamento de erros](using-macros-for-error-handling.md). 
    
MAPI_E_INVALID_PARAMETER 
  
> O membro **cValues** de uma ou mais das entradas na matriz de marca de propriedade apontado pela _lppPropTags_ é definido como 0. 
    
## <a name="remarks"></a>Comentários

Enquanto o acesso a maioria das propriedades é por identificador de propriedade, algumas propriedades podem ser acessadas pelo nome. O método **IMAPIProp::GetNamesFromIDs** pode ser chamado para fazer o seguinte: 
  
- Recupere os nomes de identificadores de propriedade específico em um conjunto específico de propriedade.
    
- Recupere os nomes de identificadores de propriedade específica em qualquer conjunto de propriedades.
    
- Recupere os nomes de todas as propriedades nomeados que estão incluídos no mapeamento do objeto.
    
Se definido de pontos de _lppPropTags_ para uma matriz de marca de propriedade válida com um ou mais identificadores de propriedade e pontos de _lpPropSetGuid_ para uma propriedade válida, **GetNamesFromIDs** ignora o conjunto de propriedades e os tipos de propriedade e retorna todos os nomes de que são mapeados para os identificadores especificados. 
  
Se for _lppPropTags_ pontos para uma matriz de marca de propriedade válida com um ou mais identificadores de propriedade e _lpPropSetGuid_ nulo, **GetNamesFromIDs** retorna todos os nomes que mapeiam para os identificadores especificados. 
  
Se um identificador especificado não tem um nome, **GetNamesFromIDs** retornará NULL no lugar do identificador na estrutura retornada em _lpppPropNames_ e também retornará MAPI_W_ERRORS_RETURNED. 
  
Se _lpPropSetGuid_ e _lppPropTags_ forem NULL, **GetNamesFromIDs** aloca uma nova matriz de marca de propriedade e retorna todos os nomes de todas as propriedades nomeadas para o objeto. 
  
Quando não houver nenhum nome a ser retornado, talvez porque não existem propriedades no conjunto de propriedade solicitada ou todas as propriedades são de um tipo excluído com os sinalizadores, **GetNamesFromIDs** faz o seguinte: 
  
- Retorna S_OK.
    
- Aloca uma nova estrutura de **SPropTagArray** , definindo o membro **cValues** como 0. 
    
- Define o conteúdo de _lpcPropNames_ como 0. 
    
- Define o conteúdo de _lpppPropNames_ como nulo. 
    
## <a name="notes-to-implementers"></a>Notas para implementadores

Se _lpPropSetGuid_ pontos para um conjunto de propriedades válido e _lppPropTags_ for nulo, o resultado é indefinido. Você pode usar uma das seguintes estratégias: 
  
- Ignorar o conjunto de propriedades e retornar os nomes para os identificadores na matriz de marca de propriedade.
    
- Retorna os nomes para apenas os identificadores da matriz de marca de propriedade que pertencem ao conjunto de propriedades especificado.
    
- Transferir a chamada, retornando MAPI_E_INVALID_PARAMETER. 
    
## <a name="notes-to-callers"></a>Notas para chamadores

Para recuperar todas as propriedades nomeadas para um objeto, você deve primeiro chamar o método do objeto [IMAPIProp::GetPropList](imapiprop-getproplist.md) e, em seguida, passa os identificadores retornados que estão acima do intervalo 0x8000 para **GetNamesFromIDs**.
  
Se você passar um conjunto de propriedades válido, mas não uma matriz de marca de propriedade válida, estar preparado para resultados imprevisíveis. Algumas implementações de **GetNamesFromIDs** ignorar o conjunto de propriedades e retornam os nomes para os identificadores na matriz de marca de propriedade. Algumas implementações retornam MAPI_E_INVALID_PARAMETER. Ainda outras implementações retornam nomes para os identificadores de todas as propriedades no conjunto de propriedades. Se o conjunto de propriedades for PS_PUBLIC_STRINGS, **GetNamesFromIDs** pode retornar todos os nomes que nunca foram criados. Se o provedor de serviço armazena uma propriedade sob os identificadores associados as cadeias de caracteres públicas é irrelevante. 
  
Quando terminar com os nomes de propriedade, verifique o conteúdo do parâmetro _lpcPropNames_ para determinar se quaisquer nomes foram retornadas. Em caso afirmativo, chame a função de [MAPIFreeBuffer](mapifreebuffer.md) para liberar a memória apontada pela _lppPropTags_ e _lpppPropNames_ quando um resultado bem-sucedido é retornado. Uma chamada de **MAPIFreeBuffer** é suficiente para cada parâmetro; Você não precisará percorrer a matriz de ponteiros e livre cada estrutura **MAPINAMEID** individualmente. 
  
Para obter mais informações sobre propriedades nomeadas, consulte [Propriedades de chamada de MAPI](mapi-named-properties.md). 
  
## <a name="mfcmapi-reference"></a>Referência MFCMAPI

Para exemplos de código MFCMAPI, consulte a tabela a seguir.
  
|**Arquivo**|**Function**|**Comment**|
|:-----|:-----|:-----|
|SingleMAPIPropListCtrl.cpp  <br/> |CSingleMAPIPropListCtrl::FindAllNamedProps  <br/> |MFCMAPI usa o método **IMAPIProp::GetNamesFromIDs** para procurar propriedades nomeadas que foram mapeadas anteriormente.  <br/> |
   
## <a name="see-also"></a>Confira também



[GUID](guid.md)
  
[IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md)
  
[IMAPIProp::GetPropList](imapiprop-getproplist.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[MAPINAMEID](mapinameid.md)
  
[SPropTagArray](sproptagarray.md)
  
[IMAPIProp : IUnknown](imapipropiunknown.md)


[MFCMAPI como um exemplo de código](mfcmapi-as-a-code-sample.md)
  
[MAPI denominada propriedades](mapi-named-properties.md)
  
[Usar macros para lidar com erros](using-macros-for-error-handling.md)

