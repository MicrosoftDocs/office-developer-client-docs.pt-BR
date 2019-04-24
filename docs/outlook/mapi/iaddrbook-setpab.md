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
ms.openlocfilehash: 29677ce74f405e8ca03f1639f3d98288532e9653
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32287011"
---
# <a name="iaddrbooksetpab"></a>IAddrBook::SetPAB

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Designa um determinado contêiner como o catálogo de endereços pessoal (PAB).
  
```cpp
HRESULT SetPAB(
  ULONG cbEntryID,
  LPENTRYID lpEntryID
);
```

## <a name="parameters"></a>Parâmetros

 _cbEntryID_
  
> no A contagem de bytes no identificador de entrada apontado pelo parâmetro _lpEntryID_ . 
    
 _lpEntryID_
  
> no Um ponteiro para o identificador de entrada do contêiner a ser designado como o PAB. O parâmetro _lpEntryID_ não pode ser nulo. 
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> O contêiner especificado foi estabelecido como o PAB.
    
## <a name="remarks"></a>Comentários

Os clientes e os provedores de serviços chamam o método **SetPAB** para designar um determinado contêiner como o PAB. O PAB é um contêiner que consiste em entradas copiadas de outros contêineres, bem como novas entradas. 
  
Uma chamada para **SetPAB** estabelece um contêiner como o PAB até que esse contêiner seja tornado indisponível ou um novo contêiner se torne o PAB por meio de uma chamada subsequente para o **SetPAB**. 
  
Os clientes e provedores não precisam chamar o método [IMAPIProp:: SaveChanges](imapiprop-savechanges.md) para tornar o PAB alterado permanentemente. 
  
## <a name="mfcmapi-reference"></a>Referência do MFCMAPI

Para ver códigos de exemplo do MFCMAPI, confira a tabela a seguir.
  
|**Arquivo**|**Função**|**Comentário**|
|:-----|:-----|:-----|
|AbContDlg. cpp  <br/> |CAbContDlg:: OnSetPAB  <br/> |MFCMAPI usa o método **SetPAB** para tornar o contêiner especificado o PAB.  <br/> |
   
## <a name="see-also"></a>Confira também



[IAddrBook::GetPAB](iaddrbook-getpab.md)
  
[IAddrBook::GetSearchPath](iaddrbook-getsearchpath.md)
  
[Propriedade canônica PidTagContainerFlags](pidtagcontainerflags-canonical-property.md)
  
[IAddrBook : IMAPIProp](iaddrbookimapiprop.md)


[MFCMAPI como exemplo de código](mfcmapi-as-a-code-sample.md)

