macaddr.js
==========
Gets the MAC addresses for the current machine.

Comes in two forms, one to get the first address found, and one to get them all.

    var macaddr = require('macaddr');
    
<strong>macaddr.address()</strong>
    
    macaddr.address(function(err, addr) {
        if (addr) {
            console.log('MAC address: ' + addr);
        } else {
            console.log('MAC address not found');
        }
    });

<strong>macaddr.all_addresses()</strong>

    macaddr.all_addresses(function(err, addrs) {
        if (addrs && addrs.length > 0) {
            console.log('MAC addresses: ' + JSON.stringify(addrs));
        } else {
            console.log('No MAC addresses found');
        }
    });
