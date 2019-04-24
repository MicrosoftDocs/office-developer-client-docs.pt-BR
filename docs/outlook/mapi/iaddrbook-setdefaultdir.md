---
title: IAddrBookSetDefaultDir
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IAddrBook.SetDefaultDir
api_type:
- COM
ms.assetid: d5d60150-15e4-41ff-bfb0-0c67e2abcacc
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 3ab01f189734ac30b4c027f4e5596c88031b5f99
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32341696"
---
# <a name="iaddrbooksetdefaultdir"></a>IAddrBook::SetDefaultDir

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Estabelece o contêiner especificado como o contêiner de catálogo de endereços padrão.
  
```cpp
HRESULT SetDefaultDir(
  ULONG cbEntryID,
  LPENTRYID lpEntryID
);
```

## <a name="parameters"></a>Parâmetros

 _cbEntryID_
  
> no A contagem de bytes no identificador de entrada apontado pelo parâmetro _lpEntryID_ . 
    
 _lpEntryID_
  
> no Um ponteiro para o identificador de entrada do contêiner de catálogo de endereços padrão.
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> O contêiner do catálogo de endereços padrão foi definido com êxito.
    
## <a name="remarks"></a>Comentários

Os clientes e os provedores de serviços chamam o método **SetDefaultDir** para estabelecer um novo contêiner de catálogo de endereços padrão. O contêiner padrão é o contêiner que o usuário vê exibido no catálogo de endereços quando o catálogo de endereços é aberto pela primeira vez. **SetDefaultDir** salva o contêiner padrão como uma entrada no perfil. O contêiner permanece como o padrão até que outra chamada para **SetDefaultDir** seja feita na mesma sessão ou em outra sessão, ou o contêiner seja removido. 
  
> [!NOTE]
> A propriedade [PR_AB_CHOOSE_DIRECTORY_AUTOMATICALLY](pidtagaddressbookchoosedirectoryautomatically-canonical-property.md) corresponde à opção **escolher automaticamente** na caixa de diálogo opções do catálogo de endereços. Quando essa propriedade existe na seção perfil do [IID_CAPONE_PROF](https://msdn.microsoft.com/library/281aabc3-9656-299c-4c78-7733dc71050a%28Office.15%29.aspx) e é definida como **true**, a caixa de diálogo catálogo de endereços não é mais padrão para o contêiner especificado por **SetDefaultDir**, mas escolhe um catálogo de endereços que o Microsoft Outlook considera apropriado para o contexto no qual a caixa de diálogo foi exibida. Observe que isso pode resultar em uma experiência ruim para provedores de catálogos de endereços de terceiros. 
  
## <a name="mfcmapi-reference"></a>Referência do MFCMAPI

Para ver códigos de exemplo do MFCMAPI, confira a tabela a seguir.
  
|**Arquivo**|**Função**|**Comentário**|
|:-----|:-----|:-----|
|Abcontdlg. cpp  <br/> |CAbContDlg:: OnSetDefaultDir  <br/> |MFCMAPI usa o método **SetDefaultDir** para tornar o contêiner de catálogo de endereços especificado o padrão.  <br/> |
   
## <a name="see-also"></a>Confira também



[IAddrBook::GetDefaultDir](iaddrbook-getdefaultdir.md)
  
[IAddrBook::GetSearchPath](iaddrbook-getsearchpath.md)
  
[IMAPISession::Logoff](imapisession-logoff.md)
  
[MAPILogonEx](mapilogonex.md)
  
[IAddrBook : IMAPIProp](iaddrbookimapiprop.md)


[MFCMAPI como exemplo de código](mfcmapi-as-a-code-sample.md)

