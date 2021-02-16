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
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 3d9c1e88b12baf50593212a3ae3c02907ce6617b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33425656"
---
# <a name="imapifoldercopyfolder"></a>IMAPIFolder::CopyFolder

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
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

## <a name="parameters"></a>Parâmetros

 _cbEntryID_
  
> [in] A contagem de byte no identificador de entrada apontado pelo parâmetro _lpEntryID._ 
    
 _lpEntryID_
  
> [in] Um ponteiro para o identificador de entrada da subpasta para copiar ou mover.
    
 _lpInterface_
  
> [in] Um ponteiro para o IID (identificador de interface) que representa a interface a ser usada para acessar a pasta à que o parâmetro  _lpDestFolder_ aponta. Passar NULL faz com que o provedor de serviços retorne a interface de pasta padrão, [IMAPIFolder : IMAPIContainer](imapifolderimapicontainer.md). Os valores válidos  _para lpInterface_ incluem IID_IUnknown, IID_IMAPIProp, IID_IMAPIContainer e IID_IMAPIFolder. 
    
 _lpDestFolder_
  
> [in] Um ponteiro para a pasta aberta para receber a subpasta copiada ou movida.
    
 _lpszNewFolderName_
  
> [in] Um ponteiro para o nome da pasta copiada ou movida em seu novo destino. Se  _lpszNewFolderName_ for definido como NULL, o nome da subpasta de origem será usado para o nome da pasta de destino. 
    
 _ulUIParam_
  
> [in] Um alça para a janela pai do indicador de progresso. O  _parâmetro ulUIParam é_ ignorado, a menos que o sinalizador FOLDER_DIALOG no parâmetro  _ulFlags_ esteja definido. 
    
 _lpProgress_
  
> [in] Um ponteiro para um objeto de progresso que exibe um indicador de progresso. Se NULL for passado  _em lpProgress_, o provedor de armazenamento de mensagens exibirá um indicador de progresso usando a implementação de objeto de progresso MAPI. O  _parâmetro lpProgress_ é ignorado, a menos que o sinalizador FOLDER_DIALOG seja definido em  _ulFlags_.
    
 _ulFlags_
  
> [in] Uma máscara de bits de sinalizadores que controla a operação de cópia ou movimentação. Os sinalizadores a seguir podem ser definidos:
    
COPY_SUBFOLDERS 
  
> Todas as subpastas na subpasta a serem copiadas também devem ser copiadas. Quando COPY_SUBFOLDERS não estiver definida para uma operação de cópia, somente a subpasta identificada por  _lpEntryID_ será copiada. Com uma operação de movimentação, o COPY_SUBFOLDERS padrão é o padrão, independentemente de o sinalizador ser definido. 
    
FOLDER_DIALOG 
  
> Solicita a exibição de um indicador de progresso.
    
FOLDER_MOVE 
  
> A subpasta deve ser movida em vez de copiada. Se FOLDER_MOVE não estiver definida, a subpasta será copiada.
    
MAPI_DECLINE_OK 
  
> Informa o provedor de armazenamento de mensagens que, se implementar **CopyFolder** chamando o método [IMAPISupport::D oCopyTo](imapisupport-docopyto.md) ou [IMAPISupport::D oCopyProps](imapisupport-docopyprops.md) do objeto de suporte, **CopyFolder** deverá retornar imediatamente MAPI_E_DECLINE_COPY. 
    
MAPI_UNICODE 
  
> O nome da pasta de destino está no formato Unicode. Se o MAPI_UNICODE não estiver definido, o nome da pasta está no formato ANSI.
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> A pasta especificada foi copiada ou movida com êxito.
    
MAPI_E_BAD_CHARWIDTH 
  
> O sinalizador MAPI_UNICODE de mensagem foi definido e o provedor de armazenamento de mensagens não oferece suporte a Unicode ou MAPI_UNICODE não foi definido e o provedor de armazenamento de mensagens suporta somente Unicode.
    
MAPI_E_COLLISION 
  
> O nome da pasta que está sendo movida ou copiada é igual ao de uma subpasta na pasta de destino. O provedor de armazenamento de mensagens exige nomes de pasta exclusivos.
    
MAPI_E_DECLINE_COPY 
  
> O provedor implementa esse método chamando um método de objeto de suporte e o chamador passou o sinalizador MAPI_DECLINE_OK suporte.
    
MAPI_E_FOLDER_CYCLE 
  
> A pasta de origem, direta ou indiretamente, contém a pasta de destino. Um trabalho significativo pode ter sido realizado antes dessa condição ser descoberta, portanto, a pasta de origem e destino pode ser parcialmente modificada. 
    
MAPI_W_PARTIAL_COMPLETION 
  
> A chamada foi bem-sucedida, mas nem todas as entradas foram copiadas com êxito. Quando esse aviso é retornado, a chamada deve ser tratada como bem-sucedida. Para testar esse aviso, use a **HR_FAILED** macro. Para obter mais informações, consulte [Usando macros para tratamento de erros.](using-macros-for-error-handling.md)
    
## <a name="remarks"></a>Comentários

O **método IMAPIFolder::CopyFolder** copia ou move uma subpasta de um local para outro. A subpasta que está sendo copiada ou movida é adicionada à pasta de destino como uma subpasta. 
  
## <a name="notes-to-implementers"></a>Observações para implementadores

Quando a operação de copiar ou mover envolve mais de uma pasta, conforme indicado pela definição do sinalizador COPY_SUBFOLDERS, execute a operação o mais completamente possível para cada pasta. Às vezes, uma das pastas a serem movidas ou copiadas não existe ou já foi movida ou copiada para outro lugar. Não pare a operação prematuramente, a menos que ocorra uma falha que esteja além do controle, como falta de memória, falta de espaço em disco ou corrupção no armazenamento de mensagens.
  
Tente manter todos os identificadores de entrada de mensagem nas mensagens copiadas. Você também deve tentar preservar identificadores de entrada, mas isso não é necessário. 
  
## <a name="notes-to-callers"></a>Notas para chamadores

Espere esses valores de retorno sob as seguintes condições.
  
|**Condition**|**Valor de retorno**|
|:-----|:-----|
|**CopyFolder** copiou ou moveu com êxito todas as mensagens e subpastas.  <br/> |S_OK  <br/> |
|**CopyFolder** não pôde copiar ou mover todas as mensagens e subpastas com êxito.  <br/> |MAPI_W_PARTIAL_COMPLETION ou MAPI_E_NOT_FOUND  <br/> |
|**CopyFolder** não pôde ser concluída.  <br/> |Qualquer valor de erro, exceto MAPI_E_NOT_FOUND  <br/> |
   
Quando **o CopyFolder** não puder ser concluído, não suponha que nenhum trabalho foi feito. **CopyFolder** pode ter sido capaz de copiar ou mover uma ou mais das mensagens e subpastas antes de encontrar o erro. 
  
Se um identificador de entrada para uma pasta que não existe for passado em  _lpEntryID_, **CopyFolder** retornará MAPI_W_PARTIAL_COMPLETION ou MAPI_E_NOT_FOUND, dependendo da implementação do armazenamento de mensagens. 
  
Dependendo do provedor de armazenamento de mensagens, o identificador de entrada da mensagem original pode ou não ser preservado na mensagem copiada. Você deve preservar os identificadores de entrada sempre que possível, mas isso não é um requisito. Geralmente, você pode depender dos seguintes cenários:
  
- Quando você move uma pasta entre dois tipos diferentes de armazenamentos de mensagens, o identificador de entrada tem garantia de alteração.
    
- Quando você move uma pasta entre dois armazenamentos de mensagens do mesmo tipo, o identificador de entrada quase sempre muda.
    
- Quando você move uma pasta para outro local no mesmo armazenamento de mensagens, o identificador de entrada pode ou não mudar, dependendo do provedor do armazenamento de mensagens.
    
## <a name="mfcmapi-reference"></a>Referência do MFCMAPI

Para ver códigos de exemplo do MFCMAPI, confira a tabela a seguir.
  
|**Arquivo**|**Função**|**Comentário**|
|:-----|:-----|:-----|
|MsgStoreDlg.cpp  <br/> |CMsgStoreDlg::OnPasteFolder  <br/> |MFCMAPI usa o **método IMAPIFolder::CopyFolder** para copiar pastas de um local para outro. MFCMAPI lembra a pasta de origem durante a operação de cópia e, na verdade, executa a cópia durante a operação de colar.  <br/> |
   
## <a name="see-also"></a>Confira também



[IMAPIFolder : IMAPIContainer](imapifolderimapicontainer.md)


[MFCMAPI como exemplo de código](mfcmapi-as-a-code-sample.md)

