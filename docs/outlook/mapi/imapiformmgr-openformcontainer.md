---
title: IMAPIFormMgrOpenFormContainer
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFormMgr.OpenFormContainer
api_type:
- COM
ms.assetid: df02bdc5-903a-4ce2-9f43-5f4513ea19b3
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 64031725e06a949464e7bfabb0a2f114d325470e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19767051"
---
# <a name="imapiformmgropenformcontainer"></a>IMAPIFormMgr::OpenFormContainer

  
  
**Aplica-se a**: Outlook 
  
Abre uma interface [IMAPIFormContainer](imapiformcontaineriunknown.md) para um contêiner de formulário específico. 
  
```cpp
HRESULT OpenFormContainer(
  HFRMREG hfrmreg,
  LPUNKNOWN lpunk,
  LPMAPIFORMCONTAINER FAR * lppfcnt
);
```

## <a name="parameters"></a>Parâmetros

 _hfrmreg_
  
> [in] Uma enumeração HFRMREG que indica a biblioteca de formulários para abrir (ou seja, o contêiner de formulário para abrir). Uma enumeração de HFRMREG é uma enumeração que é específica para um provedor de biblioteca de formulário. Os valores possíveis HFRMREG incluem o seguinte:
    
HFRMREG_DEFAULT 
  
> Um contêiner de forma conveniente.
    
HFRMREG_FOLDER 
  
> Um contêiner de pasta. 
    
HFRMREG_PERSONAL 
  
> O contêiner para o armazenamento de mensagens padrão. 
    
HFRMREG_LOCAL 
  
> Um contêiner de local do formulário. 
    
 _lpunk_
  
> [in] Um ponteiro para o objeto para o qual a interface é aberta. O parâmetro _lpunk_ deve ser **Nulo** , a menos que o valor do parâmetro _hfrmreg_ requer um ponteiro de objeto. 
    
 _lppfcnt_
  
> [out] Um ponteiro para um ponteiro para o objeto de contêiner do formulário retornado.
    
## <a name="return-value"></a>Valor retornado

S_OK 
  
> A chamada foi bem-sucedida e retornou o valor esperado ou valores.
    
MAPI_E_NO_INTERFACE 
  
> O objeto apontado pela _lpunk_ não suporta a interface necessária. 
    
## <a name="remarks"></a>Comentários

Visualizadores de formulário chame o método de **IMAPIFormMgr::OpenFormContainer** para abrir uma interface **IMAPIFormContainer** para um contêiner de formulário específico. Essa interface, em seguida, pode ser usado para instalar em e remoção de formulários do contêiner de um formulário. 
  
## <a name="notes-to-callers"></a>Notas para chamadores

Se o valor em _hfrmreg_ for HFRMREG_FOLDER, o identificador de interface usado em _lpunk_ deve ser não - **Nulo** e deve permitir chamadas de métodos [IUnknown:: QueryInterface](http://msdn.microsoft.com/en-us/library/ms682521%28v=VS.85%29.aspx) para uma interface [IMAPIFolder](imapifolderimapicontainer.md) . 
  
Para abrir o contêiner de formulário local, você deve usar uma chamada ao método **OpenFormContainer** ou a função [MAPIOpenLocalFormContainer](mapiopenlocalformcontainer.md) ; Você não pode usar o método de [IMAPIFormMgr::SelectFormContainer](imapiformmgr-selectformcontainer.md) para permitir que o usuário selecionar o contêiner de local do formulário. 
  
## <a name="mfcmapi-reference"></a>Referência MFCMAPI

Para exemplos de código MFCMAPI, consulte a tabela a seguir.
  
|**Arquivo**|**Function**|**Comment**|
|:-----|:-----|:-----|
|MainDlg.cpp  <br/> |CMainDlg::OnOpenFormContainer  <br/> |MFCMAPI usa o método **IMAPIFormMgr::OpenFormContainer** para recuperar um contêiner de formulário para que o conteúdo do contêiner pode ser renderizado.  <br/> |
|MsgStoreDlg.cpp  <br/> |CMsgStoreDlg::OnOpenFormContainer  <br/> |MFCMAPI usa o método **IMAPIFormMgr::OpenFormContainer** para recuperar um contêiner de formulário para uma pasta, para que o conteúdo do contêiner pode ser renderizado.  <br/> |
   
## <a name="see-also"></a>Confira também



[IMAPIFormContainer::InstallForm](imapiformcontainer-installform.md)
  
[IMAPIFormMgr::SelectFormContainer](imapiformmgr-selectformcontainer.md)
  
[MAPIOpenLocalFormContainer](mapiopenlocalformcontainer.md)
  
[IMAPIFormMgr : IUnknown](imapiformmgriunknown.md)


[MFCMAPI como um exemplo de código](mfcmapi-as-a-code-sample.md)

