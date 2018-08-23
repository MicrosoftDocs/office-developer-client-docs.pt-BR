---
title: IAddrBookSetPAB
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IAddrBook.SetPAB
api_type:
- COM
ms.assetid: 75daf9d4-6975-435f-91e5-1b41e0047ab7
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 461b59ff4f4c8a93f3a9945b05e31aef9a2997bf
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22569299"
---
# <a name="iaddrbooksetpab"></a>IAddrBook::SetPAB

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Designa um contêiner específico como o catálogo de endereços pessoal (PAB).
  
```cpp
HRESULT SetPAB(
  ULONG cbEntryID,
  LPENTRYID lpEntryID
);
```

## <a name="parameters"></a>Parâmetros

 _cbEntryID_
  
> [in] A contagem de bytes no identificador de entrada apontado pelo parâmetro _lpEntryID_ . 
    
 _lpEntryID_
  
> [in] Um ponteiro para o identificador de entrada do contêiner que será designado como o PAB. O parâmetro _lpEntryID_ não pode ser NULL. 
    
## <a name="return-value"></a>Valor retornado

S_OK 
  
> O contêiner especificado como o PAB foi estabelecido.
    
## <a name="remarks"></a>Comentários

Clientes e provedores de serviços de chamar o método de **SetPAB** para designar um contêiner específico como o PAB. O PAB é um contêiner que consiste de entradas copiadas de outros contêineres, bem como novas entradas. 
  
Uma chamada para **SetPAB** estabelece um contêiner como o PAB até contêiner em questão se tornar indisponível ou um novo contêiner se torna o PAB por meio de uma chamada subsequente **SetPAB**. 
  
Clientes e provedores não precisará chamar o método [IMAPIProp::SaveChanges](imapiprop-savechanges.md) para tornar a alteração PAB permanente. 
  
## <a name="mfcmapi-reference"></a>Referência MFCMAPI

Para exemplos de código MFCMAPI, consulte a tabela a seguir.
  
|**Arquivo**|**Function**|**Comment**|
|:-----|:-----|:-----|
|AbContDlg.cpp  <br/> |CAbContDlg::OnSetPAB  <br/> |MFCMAPI usa o método **SetPAB** para tornar o contêiner especificado do PAB.  <br/> |
   
## <a name="see-also"></a>Confira também



[IAddrBook::GetPAB](iaddrbook-getpab.md)
  
[IAddrBook::GetSearchPath](iaddrbook-getsearchpath.md)
  
[Propriedade canônica PidTagContainerFlags](pidtagcontainerflags-canonical-property.md)
  
[IAddrBook : IMAPIProp](iaddrbookimapiprop.md)


[MFCMAPI como um exemplo de código](mfcmapi-as-a-code-sample.md)

