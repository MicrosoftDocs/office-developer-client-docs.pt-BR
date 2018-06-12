---
title: IMAPIFolderCopyFolder
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFolder.CopyFolder
api_type:
- COM
ms.assetid: 2c1c25c6-1aec-4d9e-a2a3-bf1b4a2908b8
description: '�ltima altera��o: segunda-feira, 9 de mar�o de 2015'
ms.openlocfilehash: 5961e7a2118a46bdc9c0e66138363976ae2f7154
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19766969"
---
# <a name="imapifoldercopyfolder"></a>IMAPIFolder::CopyFolder

  
  
**Aplica-se a**: Outlook 
  
Copia ou move uma subpasta.
  
```cpp
HRESULT CopyFolder(
  ULONG cbEntryID,
  LPENTRYID lpEntryID,
  LPCIID lpInterface,
  LPVOID lpDestFolder,
  LPSTR lpszNewFolderName,
  ULONG_PTR ulUIParam,
  LPMAPIPROGRESS lpProgress,
  ULONG ulFlags
);
```

## <a name="parameters"></a>Par�metros

 _cbEntryID_
  
> [in] A contagem de bytes no identificador de entrada apontado pelo parâmetro _lpEntryID_ . 
    
 _lpEntryID_
  
> [in] Um ponteiro para o identificador de entrada da subpasta para copiar ou mover.
    
 _lpInterface_
  
> [in] Um ponteiro para o identificador de interface (IID) que representa a ser usado para acessar a pasta em que o parâmetro _lpDestFolder_ aponta para a interface. Passar NULL faz com que o provedor de serviços retornar a interface de pasta padrão, [IMAPIFolder: IMAPIContainer](imapifolderimapicontainer.md). Os valores válidos para _lpInterface_ incluem IID_IUnknown, IID_IMAPIProp, IID_IMAPIContainer e IID_IMAPIFolder. 
    
 _lpDestFolder_
  
> [in] Um ponteiro para a pasta aberta para receber a subpasta copiada ou movida.
    
 _lpszNewFolderName_
  
> [in] Um ponteiro para o nome da pasta no seu novo destino copiado ou movido. Se _lpszNewFolderName_ for definido como NULL, o nome da subpasta fonte é usado para o nome da pasta de destino. 
    
 _ulUIParam_
  
> [in] Um identificador para a janela pai do indicador de progresso. O parâmetro _ulUIParam_ é ignorado, a menos que o sinalizador FOLDER_DIALOG no parâmetro _ulFlags_ está definido. 
    
 _lpProgress_
  
> [in] Um ponteiro para um objeto de progresso que exibe um indicador de progresso. Se NULL for passado _lpProgress_, o provedor de armazenamento de mensagem exibe um indicador de progresso usando a implementação de objeto de progresso MAPI. O parâmetro _lpProgress_ é ignorado, a menos que o sinalizador FOLDER_DIALOG está definido na _ulFlags_.
    
 _ulFlags_
  
> [in] Uma bitmask dos sinalizadores que controla a operação de cópia ou movimentação. Sinalizadores a seguir podem ser definidos:
    
COPY_SUBFOLDERS 
  
> Todas as subpastas na subpasta a ser copiado também devem ser copiadas. Quando COPY_SUBFOLDERS não estiver definida para uma operação de cópia, somente a subpasta identificada pela _lpEntryID_ é copiada. Com uma operação de movimentação, o comportamento COPY_SUBFOLDERS é o padrão independentemente se o sinalizador está definido. 
    
FOLDER_DIALOG 
  
> Solicita a exibição de um indicador de progresso.
    
FOLDER_MOVE 
  
> A subpasta deve ser movido, em vez de copiados. Se FOLDER_MOVE não estiver definida, a subpasta será copiada.
    
MAPI_DECLINE_OK 
  
> Informa que o provedor de armazenamento de mensagem que se ele implementa **CopyFolder** chamando o método do objeto seu suporte de [IMAPISupport::DoCopyTo](imapisupport-docopyto.md) ou [IMAPISupport::DoCopyProps](imapisupport-docopyprops.md) , **CopyFolder** deve em vez disso imediatamente retornar MAPI_E_ DECLINE_COPY. 
    
MAPI_UNICODE 
  
> O nome da pasta de destino está no formato Unicode. Se o sinalizador MAPI_UNICODE não estiver definido, o nome da pasta é no formato ANSI.
    
## <a name="return-value"></a>Valor retornado

S_OK 
  
> A pasta especificada foi copiada ou movida com êxito.
    
MAPI_E_BAD_CHARWIDTH 
  
> Tanto o sinalizador MAPI_UNICODE foi definido e o provedor de armazenamento de mensagem não dá suporte a Unicode, ou MAPI_UNICODE não foi definido e o provedor de armazenamento de mensagem suporta somente Unicode.
    
MAPI_E_COLLISION 
  
> O nome da pasta que está sendo movido ou copiadas é igual de uma subpasta na pasta de destino. O provedor de armazenamento de mensagem requer nomes de pasta exclusivo.
    
MAPI_E_DECLINE_COPY 
  
> O provedor implemente esse método chamando um método de objeto de suporte e o chamador passou o sinalizador MAPI_DECLINE_OK.
    
MAPI_E_FOLDER_CYCLE 
  
> A pasta de origem direta ou indiretamente contém a pasta de destino. Significantes de trabalho talvez tenham sido realizadas antes que esta condição foi descoberta, para a pasta de origem e destino pode ser modificada parcialmente. 
    
MAPI_W_PARTIAL_COMPLETION 
  
> A chamada foi bem-sucedida, mas nem todas as entradas foram copiadas com êxito. Quando esse aviso é retornado, a chamada deve ser manipulada com êxito. Para testar esse aviso, use a macro **HR_FAILED** . Para obter mais informações, consulte [Usando Macros para tratamento de erros](using-macros-for-error-handling.md).
    
## <a name="remarks"></a>Coment�rios

O método **IMAPIFolder::CopyFolder** copia ou move uma subpasta de um local para outro. A subpasta a ser copiado ou movido é adicionada à pasta de destino como uma subpasta. 
  
## <a name="notes-to-implementers"></a>Notas para implementadores

Quando a operação de cópia ou movimentação envolve mais de uma pasta, conforme indicado, definindo o sinalizador COPY_SUBFOLDERS, execute a operação como completamente para cada pasta. Em alguns casos, uma das pastas a ser movido ou copiadas não existe ou já foi mudou ou copiada em outros lugares. Não interrompa a operação prematuramente, a menos que ocorre uma falha que está fora de seu controle, como ficando sem memória, ficando sem espaço em disco ou corrupção no repositório de mensagem.
  
Tente reter todos os identificadores de entrada de mensagem nas mensagens copiadas. Você também deve tentar preservar os identificadores de entrada, mas ela não é necessária. 
  
## <a name="notes-to-callers"></a>Notas para chamadores

Espera esses valores de retorno sob as condições a seguintes.
  
|**Condição**|**Valor retornado**|
|:-----|:-----|
|**CopyFolder** tem copiados ou movidos de cada mensagem e a subpasta com êxito.  <br/> |S_OK  <br/> |
|**CopyFolder** foi capaz de copiar ou mover cada mensagem e a subpasta com êxito.  <br/> |MAPI_W_PARTIAL_COMPLETION ou E_NOT_FOUND  <br/> |
|**CopyFolder** não pôde concluir.  <br/> |Qualquer valor de erro, exceto E_NOT_FOUND  <br/> |
   
Quando **CopyFolder** é impossível concluir, não presuma que foi feito nenhum trabalho. **CopyFolder** podem ter sido capaz de copiar ou mover um ou mais das mensagens e subpastas antes da ocorrência de erro. 
  
Se um identificador de entrada para uma pasta que não existe é passado _lpEntryID_, **CopyFolder** retorna MAPI_W_PARTIAL_COMPLETION ou E_NOT_FOUND, dependendo da implementação do armazenamento de mensagens. 
  
Dependendo do provedor de repositório de mensagem, o identificador de entrada da mensagem original pode ou não pode ser preservado na mensagem copiada. Você deve preservar os identificadores de entrada sempre que possível, mas não é um requisito. Geralmente, você pode depender os seguintes cenários:
  
- Quando você move uma pasta entre dois tipos diferentes de repositórios de mensagem, o identificador de entrada é garantido para alterar.
    
- Quando você move uma pasta entre dois armazenamentos de mensagem do mesmo tipo, o identificador de entrada quase sempre é alterado.
    
- Quando você move uma pasta para outro local no repositório de mensagem do mesmo, o identificador de entrada podem ou talvez não alterar, dependendo da mensagem o provedor de armazenamento.
    
## <a name="mfcmapi-reference"></a>Referência MFCMAPI

Para exemplos de código MFCMAPI, consulte a tabela a seguir.
  
|**Arquivo**|**Function**|**Comment**|
|:-----|:-----|:-----|
|MsgStoreDlg.cpp  <br/> |CMsgStoreDlg::OnPasteFolder  <br/> |MFCMAPI usa o método **IMAPIFolder::CopyFolder** para copiar pastas de um local para outro. MFCMAPI se lembra da pasta de origem durante a operação de cópia e realmente executa a cópia durante a operação de colar.  <br/> |
   
## <a name="see-also"></a>Confira também



[IMAPIFolder: IMAPIContainer](imapifolderimapicontainer.md)


[MFCMAPI como um exemplo de código](mfcmapi-as-a-code-sample.md)

