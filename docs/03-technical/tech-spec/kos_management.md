# Tech Spec — Modul `kos_management`

## 1. Metadata
- **Modul:** `kos_management`
- **Target Repo:** `kost-custom`
- **Depends:** `base`, `mail`

## 2. Models & Fields

### Model `kos.room`
- `name`: Char, required, index
- `floor`: Integer, default=1
- `room_type`: Selection [('std', 'Standard'), ('dlx', 'Deluxe'), ('vip', 'VIP')]
- `price`: Float, required
- `state`: Selection [('draft', 'Draft'), ('available', 'Available'), ('occupied', 'Occupied')]

### Model `kos.contract`
- `name`: Char, sequence/reference
- `partner_id`: Many2one 'res.partner', required
- `room_id`: Many2one 'kos.room', required
- `start_date`: Date, default=today
- `end_date`: Date
- `state`: Selection [('draft', 'Draft'), ('active', 'Active'), ('done', 'Done')]
