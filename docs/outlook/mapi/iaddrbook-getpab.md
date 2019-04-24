---
title: IAddrBookGetPAB
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IAddrBook.GetPAB
api_type:
- COM
ms.assetid: 9830e09c-700f-469b-a54d-4e4e0583aa84
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 6c565c088fd4ef7d5df141bf770c560f79535998
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32349298"
---
# <a name="iaddrbookgetpab"></a>IAddrBook::GetPAB

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Retorna o identificador de entrada do contêiner designado como o catálogo de endereços pessoal (PAB).
  
```cpp
HRESULT GetPAB(
  ULONG FAR * lpcbEntryID,
  LPENTRYID FAR * lppEntryID
);
```

## <a name="parameters"></a>Parâmetros

 _lpcbEntryID_
  
> bota Um ponteiro para a contagem de bytes no identificador de entrada apontado pelo parâmetro _lppEntryID_ . 
    
 _lppEntryID_
  
> bota Um ponteiro para um ponteiro para o identificador de entrada do PAB. O parâmetro _lppEntryID_ contém zero se nenhum contêiner tiver sido designado como o PAB. 
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> O identificador de entrada do PAB foi retornado com êxito.
    
## <a name="remarks"></a>Comentários

Os clientes chamam o método **GetPAB** para recuperar o identificador de entrada do contêiner designado como PAB. Se um PAB não foi estabelecido no perfil, MAPI seleciona como o PAB o primeiro contêiner na hierarquia de catálogo de endereços que permite modificações. 
  
## <a name="mfcmapi-reference"></a>Referência do MFCMAPI

Para ver códigos de exemplo do MFCMAPI, confira a tabela a seguir.
  
|**Arquivo**|**Função**|**Comentário**|
|:-----|:-----|:-----|
|MainDlg. cpp  <br/> |CMainDlg:: OnOpenPAB  <br/> |MFCMAPI usa o método **GetPAB** para obter a ID para o catálogo de endereços pessoal do usuário.  <br/> |
   
## <a name="see-also"></a>Confira também



[MAPIAllocateBuffer](mapiallocatebuffer.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[Propriedade canônica PidTagContainerFlags](pidtagcontainerflags-canonical-property.md)
  
[IAddrBook : IMAPIProp](iaddrbookimapiprop.md)


[MFCMAPI como exemplo de código](mfcmapi-as-a-code-sample.md)

