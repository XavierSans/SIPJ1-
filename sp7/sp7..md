# Exercici 3. Consulta de llicències de Windows Server i equips units al domini

## 1. Preu aproximat de les llicències

| Llicència | Preu aproximat |
|---|---:|
| Windows Server 2025 Standard 16 Core | 1.123,66 € sense IVA |
| Windows Server 2025 Datacenter 16 Core | 6.467,95 € sense IVA |
| Windows Server 2025 User CAL | 48,20 € sense IVA |
| Windows Server 2025 Device CAL | 37,49 € sense IVA |

Els preus són aproximats i poden variar segons el distribuïdor.

Fonts consultades:

- [Microsoft - Windows Server Pricing](https://www.microsoft.com/en-us/windows-server/pricing)
- [Microsoft - Client Access Licenses](https://www.microsoft.com/en-us/licensing/product-licensing/client-access-license)
- [Senetic - Windows Server 2025](https://www.senetic.es/category/microsoft-windows-server-2025-27154/)

---

## 2. Què és una CAL?

Una **CAL** és una **Client Access License**, és a dir, una llicència que permet que un usuari o un dispositiu pugui accedir legalment als serveis d’un servidor Windows Server.

Per exemple, una CAL permet accedir a serveis com:

- Domini
- Active Directory
- Carpetes compartides
- Impressores
- Altres recursos del servidor

### Diferència entre User CAL i Device CAL

La **User CAL** dona accés a un usuari concret, encara que aquest usuari utilitzi diferents dispositius.

La **Device CAL** dona accés a un dispositiu concret, encara que aquell dispositiu sigui utilitzat per diferents usuaris.

---

## 3. Càlcul del cost aproximat

L’empresa té:

```text
32 usuaris
25 ordinadors + 10 portàtils = 35 dispositius
```

### Cost amb User CAL

Amb **Windows Server Standard**:

```text
1 Windows Server Standard = 1.123,66 €
32 User CAL x 48,20 € = 1.542,40 €

Total = 2.666,06 € sense IVA
```

Amb **Windows Server Datacenter**:

```text
1 Windows Server Datacenter = 6.467,95 €
32 User CAL x 48,20 € = 1.542,40 €

Total = 8.010,35 € sense IVA
```

### Cost amb Device CAL

Amb **Windows Server Standard**:

```text
1 Windows Server Standard = 1.123,66 €
35 Device CAL x 37,49 € = 1.312,15 €

Total = 2.435,81 € sense IVA
```

Amb **Windows Server Datacenter**:

```text
1 Windows Server Datacenter = 6.467,95 €
35 Device CAL x 37,49 € = 1.312,15 €

Total = 7.780,10 € sense IVA
```

---

## 4. Model més adequat

El model més adequat per a aquesta empresa és el de **Device CAL**, perquè té **35 dispositius** i **32 usuaris**, però la **Device CAL és més barata** que la User CAL.

Comparant amb Windows Server Standard:

```text
User CAL = 2.666,06 €
Device CAL = 2.435,81 €
```

Per tant, el model **Device CAL** surt més econòmic:

```text
2.666,06 € - 2.435,81 € = 230,25 €
```

Així, l’empresa s’estalviaria aproximadament **230,25 € sense IVA** utilitzant **Device CAL**.

---

## 5. Mostrar els equips del domini

### Des d’Active Directory

Per veure els equips units al domini:

```text
Server Manager > Tools > Active Directory Users and Computers > Computers
```

També es pot obrir directament amb:

```text
dsa.msc
```

### Des de PowerShell

Per veure tots els equips del domini:

```powershell
Get-ADComputer -Filter *
```

Per veure-ho més ordenat:

```powershell
Get-ADComputer -Filter * -Properties OperatingSystem |
Select-Object Name, OperatingSystem, Enabled
```

Per comptar quants equips hi ha units al domini:

```powershell
(Get-ADComputer -Filter *).Count
```
