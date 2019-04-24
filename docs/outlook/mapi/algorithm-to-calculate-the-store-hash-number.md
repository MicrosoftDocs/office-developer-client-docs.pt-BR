---
title: Algoritmo para calcular o número de hash do repositório
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 489e0d74-8ecd-23ba-c874-18fd8c50fd12
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 12797c2ed96ba2db493b5cf425423ffe97fc7a5d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32331581"
---
# <a name="algorithm-to-calculate-the-store-hash-number"></a>Algoritmo para calcular o número de hash do repositório
 
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Como parte de uma URL MAPI, um provedor de armazenamento envia um número de hash do repositório para o manipulador de protocolo MAPI para identificar um objeto que está pronto para indexação. O manipulador de protocolo MAPI usa esse número de hash do repositório para identificar um repositório. Em geral, um provedor de repositório calcula o número de hash do repositório com base na assinatura de mapeamento de repositório, se o repositório tiver a propriedade **[PR_MAPPING_SIGNATURE](pidtagmappingsignature-canonical-property.md)** definida na seção global Profile. Caso contrário, o provedor da loja usará a ID de entrada da loja. O algoritmo para calcular o número de hash do repositório deve minimizar as ambigüidades que identificam os repositórios. 
  
Este tópico descreve um algoritmo que o Microsoft Office Outlook usa para calcular um número de hash do repositório com base na assinatura de mapeamento de repositório ou na ID de entrada e no nome do arquivo de repositório. 
  
O blob binário a ser codificado é o PR_ENTRYID da loja na maioria dos casos, mas para repositórios do Exchange em cache, público e privado, o blob binário deve ser o PR_MAPPING_SIGNATURE, encontrado no perfil.
  
Após calcular o hash para o blob binário de um armazenamento de pasta pública, mas antes de hash-no caminho do OST, a constante 0x2E505542, que representa a cadeia de caracteres ". PUB ", é codificada para garantir que seja exclusiva, ou seja, distinta do hash do armazenamento particular.
  
O código de suporte escolhe os bits relevantes do perfil, que podem ser usados para determinar se um repositório é público ou privado, se estiver armazenado em cache, e o caminho para o OST. Para incorporar esse código em um projeto, chame a função ComputeStoreHash, que usa como a entrada do ponteiro de sessão, bem como\_PR EntryID,\_PR SERVICE_UID e PR\_MDB_PROVIDER da tabela do repositório de mensagens. O restante das informações necessárias é do perfil. Para saída, essa função retorna o hash como calculado a partir de\_PR MAPPING_SIGNATURE se o repositório for um repositório do Exchange em cache ou o hash como computado\_de PR EntryID.
  
> [!NOTE]
> A função de suporte do HrEmsmdbUIDFromStore é uma substituição com reconhecimento de [contas do Exchange](using-multiple-exchange-accounts.md)para usar o pbGlobalProfileSectionGuid para abrir a seção de perfil de uma caixa de correio do Exchange. 
  
```cpp
#define PR_PROFILE_OFFLINE_STORE_PATH_A PROP_TAG(PT_STRING8, 0x6610)
#define PR_PROFILE_OFFLINE_STORE_PATH_W PROP_TAG(PT_UNICODE, 0x6610)
#define CONFIG_OST_CACHE_PRIVATE  ((ULONG)0x00000180)
#define CONFIG_OST_CACHE_PUBLIC   ((ULONG)0x00000400)
HRESULT HrEmsmdbUIDFromStore(IMAPISession* pmsess,
                             MAPIUID* puidService,
                             MAPIUID* pEmsmdbUID)
{
  if (!puidService) return MAPI_E_INVALID_PARAMETER;
  HRESULT hRes = S_OK;
  SRestriction mres = {0};
  SPropValue mval = {0};
  SRowSet* pRows = NULL;
  SRow* pRow = NULL;
  LPSERVICEADMIN spSvcAdmin = NULL;
  LPMAPITABLE spmtab = NULL;
  enum { eEntryID = 0, eSectionUid, eMax };
  static const SizedSPropTagArray(eMax, tagaCols) =
  {
    eMax,
    {
      PR_ENTRYID,
      PR_EMSMDB_SECTION_UID,
    }
  };
  hRes = pmsess->AdminServices(0, (LPSERVICEADMIN*)&spSvcAdmin);
  if (SUCCEEDED(hRes) && spSvcAdmin)
  {
    hRes = spSvcAdmin->GetMsgServiceTable(0, &spmtab);
    if (spmtab)
    {
      hRes = spmtab->SetColumns((LPSPropTagArray)&tagaCols, TBL_BATCH);
      mres.rt = RES_PROPERTY;
      mres.res.resProperty.relop = RELOP_EQ;
      mres.res.resProperty.ulPropTag = PR_SERVICE_UID;
      mres.res.resProperty.lpProp = &mval;
      mval.ulPropTag = PR_SERVICE_UID;
      mval.Value.bin.cb = sizeof(*puidService);
      mval.Value.bin.lpb = (LPBYTE)puidService;
      (void) spmtab->Restrict(&mres, 0);
      (void) spmtab->QueryRows(10, 0, &pRows);
      if (SUCCEEDED(hRes) && pRows && pRows->cRows)
      {
        pRow = &pRows->aRow[0];
        if (pEmsmdbUID && pRow)
        {
          if (PR_EMSMDB_SECTION_UID == pRow->lpProps[eSectionUid].ulPropTag &&
            pRow->lpProps[eSectionUid].Value.bin.cb == sizeof(*pEmsmdbUID))
          {
            memcpy(pEmsmdbUID, pRow->lpProps[eSectionUid].Value.bin.lpb, sizeof(*pEmsmdbUID));
          }
        }
      }
      FreeProws(pRows);
    }
    if (spmtab) spmtab->Release();
  }
  if (spSvcAdmin) spSvcAdmin->Release();
  return hRes;
} // HrEmsmdbUIDFromStore
bool FExchangePrivateStore(LPMAPIUID lpmapiuid)
{
  if (!lpmapiuid) return false;
  return IsEqualMAPIUID(lpmapiuid, (LPMAPIUID)pbExchangeProviderPrimaryUserGuid);
} // FExchangePrivateStore
bool FExchangePublicStore(LPMAPIUID lpmapiuid)
{
  if (!lpmapiuid) return false;
  return IsEqualMAPIUID(lpmapiuid, (LPMAPIUID)pbExchangeProviderPublicGuid);
} // FExchangePublicStore
DWORD ComputeHash(ULONG cbStoreEID, LPBYTE pbStoreEID, LPCSTR pszFileName, LPCWSTR pwzFileName, BOOL bPublicStore)
{
  DWORD  dwHash = 0;
  ULONG  cdw    = 0;
  DWORD* pdw    = NULL;
  ULONG  cb     = 0;
  BYTE*  pb     = NULL;
  ULONG  i      = 0;
  if (!cbStoreEID || !pbStoreEID) return dwHash;
  // Shouldn't see both of these at the same time.
  if (pszFileName && pwzFileName) return dwHash;
  // Get the Store Entry ID
  // pbStoreEID is a pointer to the Entry ID.
  // cbStoreEID is the size in bytes of the Entry ID.
  pdw = (DWORD*)pbStoreEID;
  cdw = cbStoreEID / sizeof(DWORD);
  for (i = 0; i < cdw; i++)
  {
    dwHash = (dwHash << 5) + dwHash + *pdw++;
  }
  pb = (BYTE *)pdw;
  cb = cbStoreEID % sizeof(DWORD);
  for (i = 0; i < cb; i++)
  {
    dwHash = (dwHash << 5) + dwHash + *pb++;
  }
  if (bPublicStore)
  {
    // Augment to assure it is unique, else could be same as private store.
    dwHash = (dwHash << 5) + dwHash + 0x2E505542; // this is '.PUB'
  }
  // To also include the store file name in the hash calculation,
  // pszFileName and pwzFileName are NULL terminated strings with the path and filename of the store.
  if (pwzFileName)
  {
    while (*pwzFileName)
    {
      dwHash = (dwHash << 5) + dwHash + *pwzFileName++;
    }
  }
  else if (pszFileName)
  {
    while (*pszFileName)
    {
      dwHash = (dwHash << 5) + dwHash + *pszFileName++;
    }
  }
  // dwHash now contains the hash to be used. It should be written in hex when building a URL.
  return dwHash;
} // ComputeHash
void ComputeStoreHash(LPMAPISESSION lpMAPISession, LPSBinary lpEntryID, LPSBinary lpServiceUID, LPSBinary lpProviderUID, DWORD* lpdwSigHash, DWORD* lpdwEIDHash)
{
  HRESULT hRes = S_OK;
  MAPIUID emsmdbUID = {0};
  LPPROFSECT lpProfSect = NULL;
  BOOL fPublicExchangeStore  = FExchangePublicStore((LPMAPIUID)lpProviderUID->lpb);
  BOOL fPrivateExchangeStore = FExchangePrivateStore((LPMAPIUID)lpProviderUID->lpb);
  BOOL fCached = false;
  LPSPropValue lpConfigProp = NULL;
  LPSPropValue lpPathPropA = NULL;
  LPSPropValue lpPathPropW = NULL;
  LPSPropValue lpMappingSig = NULL;
  LPSTR szPath = NULL; // Do not free.
  LPWSTR wzPath = NULL; // Do not free.
  // Get profile section.
  if (lpServiceUID)
  {
    hRes = HrEmsmdbUIDFromStore(lpMAPISession,
      (LPMAPIUID) lpServiceUID->lpb,
      &emsmdbUID);
    if (SUCCEEDED(hRes))
    {
      hRes = lpMAPISession->OpenProfileSection(&emsmdbUID, NULL, 0, &lpProfSect);
    }
  }
  if (!lpServiceUID || FAILED(hRes))
  {
    // For Outlook 2003/2007, HrEmsmdbUIDFromStore may not succeed,
    // so use pbGlobalProfileSectionGuid instead.
    hRes = lpMAPISession->OpenProfileSection((LPMAPIUID)pbGlobalProfileSectionGuid, NULL, 0, &lpProfSect);
  }
  if (lpProfSect)
  {
    hRes = HrGetOneProp(lpProfSect, PR_PROFILE_CONFIG_FLAGS, &lpConfigProp);
    if (SUCCEEDED(hRes) && PROP_TYPE(lpConfigProp->ulPropTag) != PT_ERROR)
    {
      if (fPrivateExchangeStore)
      {
        fCached = ((lpConfigProp->Value.l & CONFIG_OST_CACHE_PRIVATE) != 0);
      }
      if (fPublicExchangeStore)
      {
        fCached = ((lpConfigProp->Value.l & CONFIG_OST_CACHE_PUBLIC) == CONFIG_OST_CACHE_PUBLIC);
      }
    }
    if (fCached)
    {
      hRes = HrGetOneProp(lpProfSect, PR_PROFILE_OFFLINE_STORE_PATH_W, &lpPathPropW);
      if (FAILED(hRes))
      {
        hRes = HrGetOneProp(lpProfSect, PR_PROFILE_OFFLINE_STORE_PATH_A, &lpPathPropA);
      }
      if (SUCCEEDED(hRes))
      {
        if (lpPathPropW && lpPathPropW->Value.lpszW)
        {
          wzPath = lpPathPropW->Value.lpszW;
        }
        else if (lpPathPropA && lpPathPropA->Value.lpszA)
        {
          szPath = lpPathPropA->Value.lpszA;
        }
      }
      // If this is an Exchange store with an OST path, it's an OST, so get the mapping signature.
      if ((fPrivateExchangeStore || fPublicExchangeStore) && (wzPath || szPath))
      {
        hRes = HrGetOneProp(lpProfSect, PR_MAPPING_SIGNATURE, &lpMappingSig);
      }
    }
  }
  DWORD dwSigHash = NULL;
  if (lpMappingSig && PT_BINARY == PROP_TYPE(lpMappingSig->ulPropTag))
  {
    dwSigHash = ComputeHash(lpMappingSig->Value.bin.cb, lpMappingSig->Value.bin.lpb, NULL, NULL, fPublicExchangeStore);
  }
  DWORD dwEIDHash = ComputeHash(lpEntryID->cb, lpEntryID->lpb, szPath, wzPath, fPublicExchangeStore);
  if (lpdwSigHash) *lpdwSigHash = dwSigHash;
  if (lpdwEIDHash) *lpdwEIDHash = dwEIDHash;
  MAPIFreeBuffer(lpMappingSig);
  MAPIFreeBuffer(lpPathPropA);
  MAPIFreeBuffer(lpPathPropW);
  MAPIFreeBuffer(lpConfigProp);
  if (lpProfSect) lpProfSect->Release();
} // ComputeStoreHash
```

> [!TIP]
> A função HrEmsmdbUIDFromStore funciona sem realmente abrir o repositório, portanto, é uma boa abordagem de uso geral. No enTanto, se você já tiver um ponteiro para o objeto Store, também poderá recuperar o GUID da seção de perfil diretamente do repositório de mensagens lendo a propriedade PR_EMSMDB_SECTION_UID. 
  
## <a name="see-also"></a>Confira também

- [Sobre a indexação de repositórios baseados em notificação](about-notification-based-store-indexing.md)
- [Sobre URLs MAPI para indexação baseada em notificação](about-mapi-urls-for-notification-based-indexing.md)

