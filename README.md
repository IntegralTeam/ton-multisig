# ton-multisig usage

func ../stdlib.fc ./multisig-wallet-code.fc -P -o multisig-wallet-code.fif

fift -s ./new-multisig-wallet.fif <keys_num> <neccessary_sigs_num> <workchain_id> <generate_new_keys?> <filename-base> (if generate_new_keys=1, script will create new keys and save it to the filename-base, if generate_new_keys=0, script will read private keys from filename-base)

fift -s ./create-multisig-order.fif <wallet_addr> <dest_addr> <seq_no> <amount> <order_timelife_sec> [-C "comment"] [-B <boc-file>] <output-filename-base>

fift -s ./sign-multisig-order.fif <order-filename-base> <privkey-filename-base> [-new-seqno <new_seqno>] <output-filename-base>

