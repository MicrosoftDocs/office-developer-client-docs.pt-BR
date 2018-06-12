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
description: '�ltima altera��o: segunda-feira, 9 de mar�o de 2015'
ms.openlocfilehash: 00d5b2bfc6b0c024f0ef12ce19fed90ef0af6721
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19766871"
---
# <a name="iaddrbooksetdefaultdir"></a>IAddrBook::SetDefaultDir

  
  
**Aplica-se a**: Outlook 
  
Estabelece o contêiner especificado como o contêiner de catálogo de endereços padrão.
  
```cpp
HRESULT SetDefaultDir(
  ULONG cbEntryID,
  LPENTRYID lpEntryID
);
```

## <a name="parameters"></a>Par�metros

 _cbEntryID_
  
> [in] A contagem de bytes no identificador de entrada apontado pelo parâmetro _lpEntryID_ . 
    
 _lpEntryID_
  
> [in] Um ponteiro para o identificador de entrada do contêiner de catálogo de endereços padrão.
    
## <a name="return-value"></a>Valor retornado

S_OK 
  
> O contêiner de catálogo de endereços padrão foi definido com êxito.
    
## <a name="remarks"></a>Coment�rios

Provedores de serviços e clientes chame o método de **SetDefaultDir** para estabelecer um novo contêiner de catálogo de endereços padrão. O contêiner padrão é o contêiner em que o usuário vê exibido no catálogo de endereços quando o catálogo de endereços é aberto pela primeira vez. **SetDefaultDir** salva o contêiner padrão como uma entrada no perfil. O contêiner permanece como padrão até que outra chamada para **SetDefaultDir** é feita na mesma sessão ou em outra sessão, ou o contêiner é removido. 
  
> [!NOTE]
> A propriedade [PR_AB_CHOOSE_DIRECTORY_AUTOMATICALLY](pidtagaddressbookchoosedirectoryautomatically-canonical-property.md) corresponde à configuração da **Escolha automaticamente** na caixa de diálogo Opções do catálogo de endereços. Quando essa propriedade existe na seção de perfil [IID_CAPONE_PROF](http://msdn.microsoft.com/library/281aabc3-9656-299c-4c78-7733dc71050a%28Office.15%29.aspx) e estiver definida como **true**, a caixa de diálogo Catálogo de endereços não são mais padrões para o contêiner especificado por **SetDefaultDir**, mas escolhe um catálogo de endereços que considera do Microsoft Outlook apropriada para o contexto no qual a caixa de diálogo foi exibida. Observe que isso pode resultar em uma experiência ruim para provedores de catálogo de endereços de terceiros. 
  
## <a name="mfcmapi-reference"></a>Referência MFCMAPI

Para exemplos de código MFCMAPI, consulte a tabela a seguir.
  
|**Arquivo**|**Function**|**Comment**|
|:-----|:-----|:-----|
|Abcontdlg.cpp  <br/> |CAbContDlg::OnSetDefaultDir  <br/> |MFCMAPI usa o método **SetDefaultDir** para tornar o contêiner de catálogo de endereços especificado o padrão de um.  <br/> |
   
## <a name="see-also"></a>Confira também



[IAddrBook::GetDefaultDir](iaddrbook-getdefaultdir.md)
  
[IAddrBook::GetSearchPath](iaddrbook-getsearchpath.md)
  
[IMAPISession::Logoff](imapisession-logoff.md)
  
[MAPILogonEx](mapilogonex.md)
  
[IAddrBook: IMAPIProp](iaddrbookimapiprop.md)


[MFCMAPI como um exemplo de código](mfcmapi-as-a-code-sample.md)

